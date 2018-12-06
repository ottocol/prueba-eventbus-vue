<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <Componente1/>
    <br/><br/><br/>
    <Componente2/>
  </div>
</template>

<script>
import Componente1 from './components/Componente1.vue'
import Componente2 from './components/Componente2.vue'

export default {
  name: 'app',
  components: {
    Componente1,
    Componente2
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
