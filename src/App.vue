<template>
  <div id="app">
    <Ball v-for="n in 10" :key="n"></Ball>
  </div>
</template>

<script>
import Ball from './components/HelloWorld.vue'

export default {
  name: 'app',
  components: {
    Ball
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
