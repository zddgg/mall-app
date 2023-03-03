<template>
  <view style="display: flex; justify-content: space-between">
    <view style="display: flex">
      <view style="width: 40px; height: 100px; line-height: 100px">
        <nut-checkbox v-model="checkbox1" style="height: 100px; line-height: 100px">
        </nut-checkbox>
      </view>
      <view>
        <img :src="imgStr" style="width: 100px; height: 100px"/>
      </view>
    </view>
    <view style="margin-left: 10px">
      <view style="font-size: 16px">
        <nut-ellipsis content="三星 32英寸显示器曲面 可壁挂HDMI接口 高清台式电脑游戏VA曲面显示屏幕 C32R5"
                      direction="end" rows="2">
        </nut-ellipsis>
      </view>
      <view style="display: flex; margin-top: 8px">
        <view style="display: flex;background-color: #f2f2f2;
                      border-radius: 15px;
                      padding: 2px 5px;">
          <view style="font-size: 12px">
            32英寸/电竞165HZ
          </view>
          <view>
            <icon-font name="down-arrow" size="10"></icon-font>
          </view>
        </view>
      </view>
      <view style="display: flex; margin-top: 8px">
        <nut-tag color="#f93e1e" style="margin-right: 5px">
          <view style="font-size: 12px">
            满减
          </view>
        </nut-tag>
        <nut-tag color="#f93e1e" style="margin-right: 5px">
          <view style="font-size: 12px">
            满减
          </view>
        </nut-tag>
      </view>
      <view style="margin-top: 8px; padding: 5px 10px; background: linear-gradient(90deg, #fdd7dc, #ffffff 100%); border-radius: 15px">
        <view style="font-size: 12px; color: red">
          秒杀 结束时间 03月06日 06:00
        </view>
      </view>
      <view style="display: flex; margin-top: 8px; justify-content: space-between; height: 20px">
        <nut-price :price="123.23" size="normal" :need-symbol="true"/>
        <view style="display: flex;">
          <view style="font-size: 12px; color: red; height: 20px; line-height: 20px">限购2件</view>
          <nut-input-number v-model="value" readonly button-size="20"/>
        </view>
      </view>
    </view>
  </view>
</template>

<script lang="ts" setup>
import {ref} from "vue";
import {IconFont} from "@nutui/icons-vue-taro";

const imgStr = ref('https://img10.360buyimg.com/imagetools/s370x370_jfs/t1/47181/34/17995/277133/629612b3E82f9d169/554ab34e89da0fdd.jpg');
const checkbox1 = ref(false);
const value = ref(1);
</script>

<style scoped>

</style>