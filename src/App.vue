<template>
  <div id="app">
    <!--头部组件-->
    <sellHeader></sellHeader>
    <!--选项卡-->
    <div class="tab border-1px">
      <div class="tab-item">
        <router-link to="/goods">商品</router-link>
      </div>
      <div class="tab-item">
        <router-link to="/ratings">评论</router-link>
      </div>
      <div class="tab-item">
        <router-link to="/seller">商品</router-link>
      </div>
    </div>
    <router-view></router-view>
  </div>
</template>

<script>
  import sellHeader from '@/components/header/header'
  export default {
    name: 'App',
    components:{
      sellHeader
    }
  }
</script>

<style lang="stylus">
  @import './common/stylus/mixin'
  #app
    .tab
      display:flex
      height:40px
      line-height:40px
      /*border-bottom:1px solid #ddd*/
      border-1px(rgba(7, 17, 27, 0.1))
      .tab-item
        flex:1
        text-align:center
        a
          display:block
          font-size:14px
          color: rgb(77, 85, 93)
          &.router-link-active
            color: rgb(240, 20, 20)
</style>
