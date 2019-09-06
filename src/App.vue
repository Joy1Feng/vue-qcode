<template>
  <div id="app">
    <Qcode/>
  </div>
</template>

<script>
import Qcode from './components/Qcode'

export default {
  name: 'app',
  components: {
    Qcode
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
