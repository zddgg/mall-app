<template>
  <view class="index">
    <!-- 红色背景 -->
    <view class="slider-bg"></view>

    <!-- 搜索框 -->
    <searchbar-box></searchbar-box>

    <!-- 导航 -->
    <nav-box></nav-box>

    <!-- banner 轮播图 -->
    <banner-box></banner-box>

    <!-- icons 图标 -->
    <icons></icons>

    <!-- 通知 -->
    <notice></notice>

    <!-- 秒杀 -->
    <seckill></seckill>

    <!-- 主商品区域 -->
    <main-products></main-products>

  </view>
  <my-footer></my-footer>
</template>

<script lang="ts" setup>
import {reactive} from 'vue';
import SearchbarBox from "./components/searchbarBox.vue";
import NavBox from "./components/navBox.vue";
import BannerBox from "./components/bannerBox.vue";
import Icons from "./components/icons.vue";
import Notice from "./components/notice.vue";
import Seckill from "./components/seckill.vue";
import MainProducts from "./components/mainProducts.vue";
import MyFooter from '../../components/footer/footer.vue'

const state = reactive({
  msg: '欢迎使用 NutUI4.0 开发小程序',
  msg2: '你成功了～',
  type: 'text',
  show: false,
  cover: false
});

const handleClick = (type, msg, cover = false) => {
  state.show = true;
  state.msg2 = msg;
  state.type = type;
  state.cover = cover;
};
</script>

<style lang="scss">
@import "index";
</style>
