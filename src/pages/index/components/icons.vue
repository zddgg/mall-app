<template>
  <view>
    <nut-swiper :pagination-visible="true" pagination-color="#426543" height="100px">
      <nut-swiper-item v-for="(itemArr, index) in Math.ceil(listLen / 10)">
        <nut-grid :column-num="5" :border="false">
          <nut-grid-item :text="item.name"
                         v-for="(item, index) in [...list]
                         .splice(index * 10, index < Math.ceil(listLen / 10) ? index * 10 + 10: listLen % 10)">
            <icon-font :name="item.img" height="40px" width="40px" color="#478EF2"/>
          </nut-grid-item>
        </nut-grid>
      </nut-swiper-item>
    </nut-swiper>
  </view>

  <!--  <view class="icons">-->
  <!--    <nut-swiper :pagination-visible="true" pagination-color="#426543">-->
  <!--      <nut-swiper-item>-->
  <!--        <nut-grid>-->
  <!--          <nut-grid-item-->
  <!--              v-for="(item, index) in [...list].splice(0, 10)"-->
  <!--              :key="index"-->
  <!--              :icon="item.img"-->
  <!--              :text="item.name"-->
  <!--          ></nut-grid-item>-->
  <!--        </nut-grid>-->
  <!--      </nut-swiper-item>-->
  <!--      <nut-swiper-item>-->
  <!--        <nut-grid>-->
  <!--          <nut-grid-item-->
  <!--              v-for="(item, index) in [...list].splice(10, 18)"-->
  <!--              :key="index"-->
  <!--              :icon="item.img"-->
  <!--              :text="item.name"-->
  <!--          ></nut-grid-item>-->
  <!--        </nut-grid>-->
  <!--      </nut-swiper-item>-->
  <!--    </nut-swiper>-->
  <!--  </view>-->
</template>

<script lang="ts" setup>
import {computed, ref} from 'vue';
import {IconFont} from "@nutui/icons-vue-taro";

const list = ref(
    [
      {
        img: require('../../../asset/images/icons/icon1.png'),
        name: '京东超市'
      },
      {
        img: require('../../../asset/images/icons/icon2.png'),
        name: '数码电器'
      },
      {
        img: require('../../../asset/images/icons/icon3.png'),
        name: '京东新百货'
      },
      {
        img: require('../../../asset/images/icons/icon4.png'),
        name: '京东生鲜'
      },
      {
        img: require('../../../asset/images/icons/icon5.png'),
        name: '京东到家'
      },
      {
        img: require('../../../asset/images/icons/icon6.png'),
        name: '充值缴费'
      },
      {
        img: require('../../../asset/images/icons/icon7.png'),
        name: '附近好店'
      },
      {
        img: require('../../../asset/images/icons/icon8.png'),
        name: '领券'
      },
      {
        img: require('../../../asset/images/icons/icon9.png'),
        name: '领金贴'
      },
      {
        img: require('../../../asset/images/icons/icon10.png'),
        name: 'PLUS会员'
      },
      {
        img: require('../../../asset/images/icons/icon11.png'),
        name: '京东国际'
      },
      {
        img: require('../../../asset/images/icons/icon12.png'),
        name: '京东拍卖'
      },
      {
        img: require('../../../asset/images/icons/icon13.png'),
        name: '玩3C'
      },
      {
        img: require('../../../asset/images/icons/icon14.png'),
        name: '沃尔玛'
      },
      {
        img: require('../../../asset/images/icons/icon15.png'),
        name: '美妆馆'
      },
      {
        img: require('../../../asset/images/icons/icon16.png'),
        name: '京东旅行'
      },
      {
        img: require('../../../asset/images/icons/icon17.png'),
        name: '拍拍二手'
      },
      {
        img: require('../../../asset/images/icons/icon18.png'),
        name: '潮燃青年'
      }
    ]
)

const listLen = computed(() => {
  return list.value.length;
})

console.log(listLen)

</script>

<style lang="scss">
</style>