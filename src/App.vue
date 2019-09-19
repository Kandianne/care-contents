<template>
  <div id="app">
    <a href="https://www.movinghelp.com/movers/raleigh-nc-27606/90476?agnosticDetails=False&orderType=1&jobActivityType=0">
    <img alt="Careful Contents Movers" src="./assets/logo.png">
    </a>
    <Home/>
  </div>
</template>

<script>
import Home from './components/Home.vue'

export default {
  name: 'app',
  components: {
    Home
  }
}
</script>

<style>
body {
  margin: 0px;
  height: 900px;
  overflow: hidden;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  background: #d9dada;
  margin: 0px;
  height: 100%;
  padding-top: 30%;
}
img {
  width:150px;
}
</style>
