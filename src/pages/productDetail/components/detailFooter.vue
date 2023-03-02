<template>
  <view class="detail_footer">
    <view class="icon_wrap">
      <view class="store">
        <icon-font name="shop"></icon-font>
        <view style="font-size: 12px">店铺</view>
      </view>
      <view class="service">
        <icon-font name="dongdong"></icon-font>
        <view style="font-size: 12px">客服</view>
      </view>
      <view class="cart">
        <icon-font name="cart"></icon-font>
        <view style="font-size: 12px">购物车</view>
      </view>
    </view>
    <view class="btn_wrap">
      <nut-button type="warning">加入购物车</nut-button>
      <nut-button type="primary">立即购买</nut-button>
    </view>
  </view>
</template>
<script lang="ts" setup>
import {IconFont} from "@nutui/icons-vue-taro";
</script>
<style lang="scss">
.detail_footer {
  background-color: #fff;
  border-top: 1px solid rgba(0, 0, 0, 0.1);
  height: 100px;
  position: fixed;
  bottom: 0;
  width: 100%;
  z-index: 20;
  align-items: center;
  justify-content: space-between;
  display: flex;
  padding: 0 20px;
  box-sizing: border-box;

  .icon_wrap {
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .store {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    font-size: 18px;
    margin-left: 30px;
  }

  .service {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    font-size: 18px;
    margin-left: 45px;
  }

  .cart {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    font-size: 18px;
    margin-left: 45px;
  }

  .btn_wrap {
    .nut-button:first-child {
      margin-right: 10px;
    }
  }
}
</style>
