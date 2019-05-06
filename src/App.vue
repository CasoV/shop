<template>
  <div id="app">
    <router-view></router-view>
    <van-tabbar v-model='active'>
      <van-tabbar-item icon="wap-home" to="/">首页</van-tabbar-item>
      <van-tabbar-item icon="records" to="category">分类</van-tabbar-item>
      <van-tabbar-item icon="cart" to="cart">购物车</van-tabbar-item>
      <van-tabbar-item icon="contact" to="profile">我的</van-tabbar-item>
    </van-tabbar>
    <!-- <ul class="footer-bar">
      <li class="footer-bar-item">
        <router-link to="/">首页</router-link>
      </li>
      <li class="footer-bar-item">
        <router-link to="category">分类</router-link>
        </li> 
      <li class="footer-bar-item"><router- link to="cart">购物车</router-link></li>
      <li class="footer-bar-item"><router-link to="profile">我的</router-link></li>
    </ul>-->
  </div>
</template>
<script>
export default {
  data () {
    return {
      active:0
    }
  }
}
</script>

<style lang="scss">
.footer-bar {
  display: flex;
  background: #eeeeee;
  //固定定位 最下方
  position: fixed;
  bottom: 0;
  width: 100%;
  height: 1rem;
  line-height: 1rem;
  &-item {
    flex: 1;
    text-align: center;
  }
  // flex-grow: 1; //子元素fix统一为1
  //width:0   //若子元素内容宽度不同导致flex失效
}
</style>
