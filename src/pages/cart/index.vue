<template>
  <view style="background-color: #f3f3f3; padding: 10px 0">
    <store-card style="margin: 0 10px 10px 10px; padding: 10px; border-radius: 14px" v-for="i in 5" :key="i">
    </store-card>
  </view>
  <my-footer></my-footer>
</template>

<script lang="ts" setup>
import StoreCard from "./components/storeCard.vue";
import MyFooter from '../../components/footer/footer.vue'</script>

<style scoped>

</style>