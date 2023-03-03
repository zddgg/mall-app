<template>
  <view>
    <store-card></store-card>
    <preference-card></preference-card>
    <product-card></product-card>
  </view>
  <my-footer></my-footer>
</template>

<script lang="ts" setup>
import StoreCard from "./components/storeCard.vue";
import PreferenceCard from "./components/preferenceCard.vue";
import ProductCard from "./components/productCard.vue";
import MyFooter from '../../components/footer/footer.vue'</script>

<style scoped>

</style>