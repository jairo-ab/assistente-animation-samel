<template>
  <div id="app">
    <Assistente msg="Assistente Virtual Sam"/>
  </div>
</template>

<script>
import Assistente from './components/Assistente.vue'

export default {
  name: 'App',
  components: {
    Assistente
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
