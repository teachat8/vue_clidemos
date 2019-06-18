<template>
  <div>This is Hello</div>
</template>

<script>
import Bus from '../bus'
export default {
  name: 'hello',
  mounted() {
    Bus.$on('msg', (e) => {
      console.log(e)
    })
  }
}
</script>

<style>

</style>
