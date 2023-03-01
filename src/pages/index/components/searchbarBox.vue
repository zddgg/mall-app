<template>
  <view class="search-bar-box">
    <nut-searchbar v-model="searchValue">
      <template v-slot:leftin>
        <icon-font size="14" name="search" color="#fa2c19"></icon-font>
      </template>
      <template v-slot:rightin>
        <icon-font size="20" name="photograph"></icon-font>
        <nut-divider direction="vertical"/>
        <icon-font size="20" name="scan2" color="#fa2c19" style="margin-right: 10px"></icon-font>
      </template>
    </nut-searchbar>
  </view>
</template>

<script lang="ts" setup>
import {ref} from 'vue'
import {IconFont} from "@nutui/icons-vue-taro";

const searchValue = ref('');

</script>

<style lang="scss">
</style>