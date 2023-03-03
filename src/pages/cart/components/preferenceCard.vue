<template>
  <view class="preference-card">
    <view style="margin-left: 40px; display: flex; justify-content: space-between">
      <view style="display: flex;">
        <nut-tag color="#f93e1e" size="10px">
          <view style="font-size: 10px">
            跨品类满折
          </view>
        </nut-tag>
        <view style="font-size: 12px; margin-left: 4px">满2类总价9.8折，还差1类</view>
      </view>
      <view style="font-size: 12px">
        去凑单
        <icon-font name="right" size="12px"></icon-font>
      </view>
    </view>
    <product-card style="margin-top: 10px" v-for="i in 2"></product-card>
  </view>
</template>

<script lang="ts" setup>
import {IconFont} from "@nutui/icons-vue-taro";
import ProductCard from "./productCard.vue";
</script>

<style lang="scss" scoped>
</style>