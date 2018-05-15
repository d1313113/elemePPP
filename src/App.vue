/*
 * @Author: Cumelmell
 * @Date: 2018-05-15 23:24:54
 * @Last Modified by: Cumelmell
 * @Last Modified time: 2018-05-15 23:40:05
 */
<template>
  <div id="app">
    <!-- 头部组件 -->
    <v-header :seller="seller"></v-header>
    <router-view/>
  </div>
</template>

<script type="text/ecmascript-6">
// 引入header头部组件
import header from '@/components/header/header'
// 引入数据
import data from '@/common/json/data.json'

export default {
  name: 'App',
  data () {
    return {
      seller: {}
    }
  },
  created () {
    // 数据初始化
    this.seller = data.seller
  },
  methods: {

  },
  components: {
    // 引入头部组件
    'v-header': header
  }
}
</script>
<style lang="scss" scoped>
#app{
  margin: 0;
  padding: 0;
  border: 1px solid #000;
}
</style>
