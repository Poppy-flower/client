<template>
  <div id="app">
    <router-view></router-view>
    <van-tabbar v-model="active">
      <van-tabbar-item icon="home-o" @click="handleClickHome">首页</van-tabbar-item>
      <van-tabbar-item icon="plus" @click="handleClickAdd">发布</van-tabbar-item>
    </van-tabbar>
  </div>
</template>

<script>
  import { Tabbar, TabbarItem } from 'vant';

  export default {
    name: 'App',
    components: {
      [Tabbar.name]: Tabbar,
      [TabbarItem.name]: TabbarItem,
    },
    data() {
      return {
        active: 0,
      };
    },
    methods: {
      handleClickHome(){
        this.$router.push('/');
      },
      handleClickAdd(){
        this.$router.push('/add');
      }
    }
  }
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
