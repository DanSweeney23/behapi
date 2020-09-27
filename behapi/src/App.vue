<template>
  <div id="appContainer">
    <Drum/>
  </div>
</template>

<script>
import Drum from './pages/Drum.vue'

export default {
  name: 'App',
  components: {
    Drum
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  background-color: #14035d;
  margin-top: 60px;
}
</style>
