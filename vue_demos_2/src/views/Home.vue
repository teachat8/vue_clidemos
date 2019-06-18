<template>
  <div class="home">
    <HelloWorld msg="welcome to your vuejs" @setMsg="getChildMsg"/>
    <Hello/>
  </div>
</template>

<script>
import HelloWorld from '../components/HelloWorld'
import Hello from '../components/Hello'

export default {
  name: 'home',
  components: {
    HelloWorld,
    Hello
  },
  methods: {
    getChildMsg(childMsg) {
      console.log('子组件传递过来的数据为--->>>', childMsg)
    }
  }
}
</script>

<style>

</style>
