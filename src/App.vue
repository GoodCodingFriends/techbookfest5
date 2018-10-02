<template>
  <div id="app">
    <h1>GCF Lab</h1>
    <Market/>
  </div>
</template>

<script>
import Market from './components/Market.vue'
import Media from 'vue-media'

export default {
  name: 'app',
  components: {
    Market,
    Media,
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
