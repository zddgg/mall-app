<template>
  <view id="goodsComment" class="anchor"></view>
  <view class="goods_comment">
    <view class="title_wrap">
      <view class="cart_title">
        评价
      </view>
      <view class="percent">
        好评度97%
        <icon-font name="arrow-right" size="12px"></icon-font>
      </view>
    </view>
    <view class="container">
      <view v-for="cmt in comment" class="comment_wrap">
        <nut-comment
            :images="cmt.images"
            :videos="cmt.videos"
            :info="cmt.info"
            @clickImages="clickImages"
            @clickOperate="clickOperate"
            :operation="['replay']"
        >
          <template #comment-labels>
            <img
                class="nut-comment-header__labels--item"
                src="https://storage.360buyimg.com/imgtools/78925d9440-f9e874d0-e93d-11eb-8e5c-0da9e18a13b1.png"
                style="height: 12px; width: 30px"
            />
          </template>
        </nut-comment>
      </view>
    </view>
    <view class="comment_opt">
      <nut-button type="default" size="small">查看全部评价</nut-button>
    </view>
  </view>
</template>
<script lang="ts" setup>
import {ref} from "vue";
import {IconFont} from "@nutui/icons-vue-taro";
import data from "../mock/comment.json";

const comment = ref(data.Comment);
const clickImages = (imgs) => {
  console.log("进行图片展示", imgs);
};
const clickOperate = (type) => {
  console.log(type);
};
</script>
<style lang="scss">
.goods_comment {
  background-color: #fff;
  border-radius: 12px;
  margin-top: 12px;
  padding: 12px 18px;
  position: relative;

  .title_wrap {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 20px;

    .percent {
      color: #8c8c8c;
      display: flex;
      align-items: center;
      font-size: 20px;
    }
  }

  .comment_opt {
    padding: 12px 0;
    display: flex;
    justify-content: center;
  }

  .comment_wrap {
    margin-bottom: 12px;
  }
}
</style>
