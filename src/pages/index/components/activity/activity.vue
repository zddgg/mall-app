<template>
  <view>
    <nut-grid :column-num="2" :border="false">
      <nut-grid-item v-for="i in 4">
        <activity-card :title="'京东秒杀'"></activity-card>
      </nut-grid-item>
    </nut-grid>
    <nut-grid :column-num="4" :border="false">
      <nut-grid-item v-for="i in 4">
        <activity-card :title="'京东秒杀'" :title-tag="false"></activity-card>
      </nut-grid-item>
    </nut-grid>
  </view>
</template>

<script lang="ts" setup>
import ActivityCard from './components/activityCard.vue'

</script>

<style scoped>

</style>