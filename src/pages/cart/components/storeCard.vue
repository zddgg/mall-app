<template>
  <view style="background-color: #ffffff">
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
          <icon-font name="issue" size="12"></icon-font>
        </view>
        <view style="font-size: 12px">以免运费</view>
      </view>
    </view>
    <view style="margin-top: 5px" v-for="i in 2">
      <preference-card>
      </preference-card>
      <nut-divider v-if="i<2" class="preference-divider" dashed :style="{ borderColor: '#fafafa' }"></nut-divider>
    </view>
  </view>
</template>

<script lang="ts" setup>
import {ref} from "vue";
import {IconFont} from "@nutui/icons-vue-taro";
import PreferenceCard from "./preferenceCard.vue";

const checkbox1 = ref(false);
</script>

<style scoped>

</style>