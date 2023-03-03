<template>
  <view style="background-color: #f3f3f3; padding: 10px 0; margin-bottom: 180px">
    <store-card style="margin: 0 10px 10px 10px; padding: 10px; border-radius: 14px" v-for="i in 5" :key="i">
    </store-card>
  </view>
  <view class="cart-action" style="display: flex; justify-content: space-between; padding: 5px 10px">
    <view style="display: flex">
      <nut-checkbox v-model="value">全选</nut-checkbox>
      <view style="margin-left: 10px">
        <view style="font-size: 14px">合计: ￥45.23</view>
        <view style="display: flex; font-size: 12px">
          <view>优惠减: ￥23.25</view>
          <view style="background-color: #f1f1f1;
          margin-left: 2px;
          padding: 0 5px; border-radius: 14px">优惠明细
          </view>
        </view>
      </view>
    </view>
    <view>
      <nut-button color="#ff3d46">
        <view style="color: #ffffff">去结算(18)</view>
      </nut-button>
    </view>
  </view>
  <view style="height: 100px">
  </view>
  <my-footer></my-footer>
</template>

<script lang="ts" setup>
import StoreCard from "./components/storeCard.vue";
import MyFooter from '../../components/footer/footer.vue'
import {ref} from "vue";

const value = ref(false);
</script>

<style lang="scss">
.cart-action {
  background-color: #fff;
  border-top: 1px solid rgba(0, 0, 0, 0.1);
  height: 100px;
  position: fixed;
  bottom: 170px;
  width: 100%;
  z-index: 20;
  align-items: center;
  justify-content: space-between;
  display: flex;
  padding: 0 20px;
  box-sizing: border-box;
}
</style>