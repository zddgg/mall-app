<template>
  <view style="display: flex; justify-content: space-between">
    <view style="display: flex">
      <view style="width: 40px">
        <nut-checkbox v-model="checkbox1">
        </nut-checkbox>
      </view>
      <view style="display: flex">
        <view>JD 华为自营旗舰店</view>
        <view>
          <icon-font name="right" size="12px"></icon-font>
        </view>
      </view>
    </view>
    <!--  右侧标签  -->
    <view style="display: flex">
      <view>
        <icon-font name="issue" size="20px"></icon-font>
      </view>
      <view style="font-size: 20px">以免运费</view>
    </view>
  </view>
</template>

<script lang="ts" setup>
import {ref} from "vue";
import {IconFont} from "@nutui/icons-vue-taro";

const checkbox1 = ref(false);
</script>

<style scoped>

</style>