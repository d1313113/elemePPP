<template>
  <div id="app">
    <!-- 头部组件 -->
    <v-header></v-header>
    <router-view/>
  </div>
</template>

<script>
// 引入header头部组件
import header from '@/components/header/header'

export default {
  name: 'App',
  data () {
    return {

    }
  },
  created () {

  },
  methods: {

  },
  components: {
    // 引入头部组件
    'v-header': header
  }
}
</script>

<style>
</style>
