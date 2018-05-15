/*
 * @Author: Cumelmell
 * @Date: 2018-05-15 23:30:16
 * @Last Modified by: Cumelmell
 * @Last Modified time: 2018-05-16 00:18:06
 */
<template>
  <!-- 头部容器 -->
  <div class="header">
    <!-- 头部主体 -->
    <div class="content-wrapper">
      <!-- 头像 -->
      <div class="avatar">
        <img :src="seller.avatar" alt="" width="64" height="64">
      </div>
      <!-- 右侧店家信息 -->
      <div class="content">
        <!-- 店家名字 -->
        <div class="title">
          <span class="brand"></span>
          <span class="name">{{seller.name}}</span>
        </div>
        <!-- 送货描述 -->
        <div class="description">
          {{seller.description}}/{{seller.deliveryTime}}分钟送达
        </div>
        <!-- 点击优惠满减 -->
        <div class="support">
          <span class="icon" :class="classMap[seller.supports[0].type]"></span>
          <span class="text">{{seller.supports[0].description}}</span>
        </div>
        <!-- 优惠类型 -->
        <div class="supports-count">
          几个支持
        </div>
      </div>
    </div>
    <!-- 商家滚动介绍 -->
    <div class="bulletin-wrapper">
      商家滚动介绍
    </div>
    <!-- 头部背景 -->
    <div class="background">
      头部背景
      <img src="" alt="">
    </div>
    <!-- 商家星级弹出层 -->
  </div>
</template>
<script type="text/ecmascript-6">
export default {
  props: {
    seller: {
      type: Object
    }
  },
  data () {
    return {
      detailShow: false
    }
  },
  created () {
    this.classMap = ['decrease', 'discount', 'special', 'invoice', 'guarantee']
  },
  methods: {

  }
}
</script>
<style lang="scss" scoped>
@import url('header.scss');
</style>
