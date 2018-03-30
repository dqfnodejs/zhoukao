<template>
  <div id="app">
    <zhoukao></zhoukao>
    
  </div>
</template>

<script>
import zhoukao from './components/zhoukao.vue'

export default {
  name: 'app',
  components: {
    zhoukao
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
