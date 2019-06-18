<template>
  <div class="home">
    <p>方式1.path</p>
    <button @click="goToAbout">path利用js事件传递路由参数</button>
    <br/>
    <!-- path与query方式1.使用router-link路由跳转传参 -->
    <router-link :to="{path: '/about', query: {code: '1'}}">path利用router-link传递路由参数</router-link>
    <br/>
    <p>方式2.name</p>
    <button @click="namegoToAbout">name利用js事件传递路由参数</button>
    <br/>
    <!-- name与params方式1.使用router-link路由跳转传参 -->
    <router-link :to="{name: 'about', params: {code: '2'}}">name利用router-link传递路由参数</router-link>
  </div>
</template>

<script>
export default {
  name: 'Home',
  methods: {
    // path与query方式2.js事件路由跳转传参
    goToAbout() {
      this.$router.push({
        path: '/about',
        query: {
          code: '1'
        }
      })
    },
    // name与params方式2.js事件路由跳转传参
    namegoToAbout() {
      this.$router.push({
        name: 'about',
        params: {
          code: '2'
        }
      })
    }
  }
}
</script>

<style>

</style>
