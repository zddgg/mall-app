<template>
  <view style="background-color: #f7f8fa">
    <nut-tabbar
        v-model="currentTab"
        :bottom="true"
        safe-area-inset-bottom
        unactive-color="#333"
        active-color="#f00"
        @tab-switch="tabSwitch"
    >
      <nut-tabbar-item v-for="(item,index) in tabs"
                       :key="index"
                       :tab-title="item.title"
                       @click="redirectTo(item.page)"
      >
        <template #icon>
          <icon-font v-if="currentTab === index" :name="item.activeImg"></icon-font>
          <icon-font v-else :name="item.img"></icon-font>
        </template>
      </nut-tabbar-item>
    </nut-tabbar>
  </view>
</template>

<script lang="ts" setup>
import {IconFont} from "@nutui/icons-vue-taro";
import {ref} from "vue";
import Taro from "@tarojs/taro";

const currentTab = ref(0);
const tabs = [
  {
    title: '首页',
    img: require('../../asset/images/footer/home.png'),
    activeImg: require('../../asset/images/footer/home_hover.png'),
    page: '/pages/index/index'
  },
  {
    title: '分类',
    img: require('../../asset/images/footer/category.png'),
    activeImg: require('../../asset/images/footer/category_hover.png'),
    page: '/pages/index/index'
  },
  {
    title: '附近生活圈',
    img: require('../../asset/images/footer/life.png'),
    activeImg: require('../../asset/images/footer/life_hover.png'),
    page: '/pages/index/index'
  },
  {
    title: '购物车',
    img: require('../../asset/images/footer/cart.png'),
    activeImg: require('../../asset/images/footer/cart_hover.png'),
    page: '/pages/cart/index'
  },
  {
    title: '我的',
    img: require('../../asset/images/footer/my.png'),
    activeImg: require('../../asset/images/footer/my_hover.png'),
    page: '/pages/index/index'
  }
]

function tabSwitch(item, index) {
  console.log(item, index);
}

const redirectTo = (page) => {
  // 跳转到目的页面，打开新页面
  Taro.redirectTo({
    url: page,
  })
}

</script>

<style scoped>

</style>