<template>
  <view class="banner">
    <nut-swiper
        :pagination-visible="true"
        pagination-color="#426543"
        auto-play="3000">
      <nut-swiper-item
          v-for="(banner, index) in banners"
          :key="index"
          @click="handleGo(banner.link)">
        <img :src="banner.img" alt=""/>
      </nut-swiper-item>
    </nut-swiper>
  </view>
</template>

<script lang="ts" setup>
import {ref} from 'vue'

const banners = ref(
    [
      {
        img: require('../../../asset/images/banners/banner1.jpg'),
        link: 'https://www.jd.com'
      },
      {
        img: require('../../../asset/images/banners/banner2.jpg'),
        link: 'https://www.jd.com'
      },
      {
        img: require('../../../asset/images/banners/banner3.jpg'),
        link: 'https://www.jd.com'
      },
      {
        img: require('../../../asset/images/banners/banner4.jpg'),
        link: 'https://www.jd.com'
      },
      {
        img: require('../../../asset/images/banners/banner5.jpg'),
        link: 'https://www.jd.com'
      },
      {
        img: require('../../../asset/images/banners/banner6.jpg'),
        link: 'https://www.jd.com'
      }
    ]
)

const handleGo = link => {
  location.href = link
}
</script>

<style lang="scss">
</style>