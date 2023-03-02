<template>
  <view class="activity-card">
    <view class="activity-card-header">
      <view class="activity-card-header-text">
        {{ title }}
      </view>
      <view v-if="titleTag" class="activity-card-header-tag">
        <nut-tag color="#FA685D">
          限时特惠
        </nut-tag>
      </view>
    </view>
    <view class="activity-card-header-extra">
      大家都在买
    </view>
    <view class="activity-card-content">
      <img :src="img"/>
      <view class="activity-card-content-extra">
        <nut-price size="small" :price="10010.01" symbol="¥"/>
      </view>
    </view>
    <view class="activity-card-footer">
    </view>
  </view>
</template>

<script lang="ts" setup>
defineProps({
  title: {
    type: String,
    default: ''
  },
  titleTag: {
    type: Boolean,
    default: true
  }
})
const img = require('../../../../../../src/asset/images/seckillProducts/product1.jpeg')
</script>

<style lang="scss">
.activity-card {
  width: 100%;
  height: 100%;
  .activity-card-header {
    display: flex;
    .activity-card-header-text {
      font-weight: bold;
    }

    .activity-card-header-tag {
      margin-left: 10px;
      font-weight: bold;
    }
  }

  .activity-card-header-extra {
    margin-top: 5px;
    color: #fb258d;
    font-size: .9rem;
  }

  &-image {
    width: 100%;
    height: 300px;
    border-radius: 10px;
    overflow: hidden;
    margin-bottom: 8px;

    img {
      width: 100%;
      height: 100%;
    }
  }

  .activity-card-content {
    width: 100%;
    height: 150px;
    border-radius: 10px;
    overflow: hidden;
    margin-top: 15px;
    img {
      width: 100%;
      height: 100%;
    }

    .activity-card-content-extra {
      text-align: center;
    }
  }
}
</style>