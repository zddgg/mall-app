<template>
  <view class="goods_detail">
    <!-- 顶部导航 -->
    <top-nav></top-nav>
    <!-- 商品基本信息 -->
    <goods-info></goods-info>
    <!-- 商品规格选择 -->
    <goods-sku></goods-sku>
    <!-- 地址信息 -->
    <address-info></address-info>
    <!-- 推荐列表 -->
    <recommend-list></recommend-list>
    <!-- 评论信息 -->
    <goods-comment></goods-comment>
    <!-- 商品详情 -->
    <more-detail></more-detail>
    <!-- 底部操作 -->
    <detail-footer></detail-footer>
  </view>
</template>

<script lang="ts" setup>
import {ref} from "vue";
import TopNav from "./components/topNav.vue";
import GoodsInfo from "./components/goodsInfo.vue";
import GoodsSku from "./components/goodsSku.vue";
import AddressInfo from "./components/addressInfo.vue";
import RecommendList from "./components/recommendList.vue";
import GoodsComment from "./components/goodsComment.vue";
import MoreDetail from "./components/moreDetail.vue";
import DetailFooter from "./components/detailFooter.vue";

const text = ref('北京大兴区亦庄经济开发区科创十一街与经海四路交叉口西北150米京东总部4号楼');
</script>
<style lang="scss">
//@import "index";

.goods_detail {
  height: 100%;
  width: 100%;
  background: #f3f3f3;
  overflow-y: auto;
  overflow-x: hidden;
  box-sizing: border-box;
  padding-bottom: 70px;

  .nut-ellipsis {
    flex: 1;
    margin-left: 4px;
    min-width: 200px;
  }
}
</style>
