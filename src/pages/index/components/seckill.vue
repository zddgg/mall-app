<template>
<!--  <view class="seckill">-->
<!--    <view class="seckill-top">-->
<!--      <view class="seckill-title-countdown">-->
<!--        <view class="seckill-title">京东秒杀</view>-->
<!--        <view class="seckill-countdown">-->
<!--          <view class="seckill-countdown-type">12点场</view>-->
<!--          <nut-countdown :end-time="end"/>-->
<!--        </view>-->
<!--      </view>-->
<!--      <view class="seckill-arrow-box">爆款轮番秒-->
<!--        <icon-font name="arrow-right" size="11"/>-->
<!--      </view>-->
<!--    </view>-->
<!--    <view class="seckill-bottom">-->
<!--      <view v-for="(product, index) in seckillProducts" :key="index" class="seckill-product">-->
<!--        <view>-->
<!--          <img :src="product.img"/>-->
<!--        </view>-->
<!--        <view class="seckill-product-price">¥{{ product.price }}</view>-->
<!--      </view>-->
<!--    </view>-->
<!--  </view>-->
  <view>
    <activity></activity>
  </view>
</template>

<script lang="ts" setup>
import {reactive, ref} from 'vue'
import Activity from '../components/activity/activity.vue'
import {IconFont} from "@nutui/icons-vue-taro";

const end = ref(Date.now() + 60 * 1000)

const seckillProducts = reactive(
    [
      {
        img: require('../../../asset/images/seckillProducts/product1.jpeg'),
        price: 11.99
      },
      {
        img: require('../../../asset/images/seckillProducts/product1.jpeg'),
        price: 11.99
      },
      {
        img: require('../../../asset/images/seckillProducts/product1.jpeg'),
        price: 11.99
      },
      {
        img: require('../../../asset/images/seckillProducts/product1.jpeg'),
        price: 11.99
      },
      {
        img: require('../../../asset/images/seckillProducts/product1.jpeg'),
        price: 11.99
      },
      {
        img: require('../../../asset/images/seckillProducts/product1.jpeg'),
        price: 11.99
      }
    ]
);
</script>

<style lang="scss">
</style>