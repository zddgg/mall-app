<template>
  <view class="main-products" @click="goDetail">
    <view
        v-for="(mainProduct, index) in mainProducts"
        :key="index"
        class="main-product"
    >
      <view class="main-product-image">
        <img :src="mainProduct.img"/>
      </view>
      <view class="main-product-name">{{ mainProduct.name }}</view>
      <nut-price
          :price="10010.01"
          :need-symbol="true"
          size="normal"
          :thousands="false"
      />
      <view class="comment-points">
        <view class="comment">{{ mainProduct.comments }}条评论</view>
        <view class="points">
          <view class="point"></view>
          <view class="point"></view>
          <view class="point"></view>
        </view>
      </view>
    </view>
  </view>
</template>

<script lang="ts" setup>
import {reactive} from "vue";
import Taro from "@tarojs/taro"
import data from "./mock.json";

const mainProducts = reactive(data.mainProducts);
const goDetail = () => {
  Taro.navigateTo({
    url: "/pages/productDetail/index",
  });
};

</script>

<style lang="scss">
</style>