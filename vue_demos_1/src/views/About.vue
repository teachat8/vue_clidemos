<template>
  <div class="about">
    <router-link to="/">返回Home页面</router-link>
    <h1>This is an about page</h1>
  </div>
</template>

<script>
export default {
  name: 'About',
  mounted() {
    console.log(111)
    console.log('方式1.path方式接受参数', this.$route.query.code)
    console.log('方式2', this.$route.params.code)
  }
}
</script>

<style>

</style>
