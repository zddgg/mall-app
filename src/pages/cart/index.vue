<template>
  <view>
    <nut-grid :column-num="2">
      <nut-grid-item v-for="i in 4">
        <activity-card :title="'京东秒杀'"></activity-card>
      </nut-grid-item>
    </nut-grid>
    <nut-grid :column-num="4">
      <nut-grid-item v-for="i in 4">
        <activity-card :title="'京东秒杀'" :title-tag="false"></activity-card>
      </nut-grid-item>
    </nut-grid>
  </view>
  <my-footer></my-footer>
</template>

<script lang="ts" setup>
import ActivityCard from '../index/components/activity/components/activityCard.vue'
import MyFooter from '../../components/footer/footer.vue'</script>

<style scoped>

</style>