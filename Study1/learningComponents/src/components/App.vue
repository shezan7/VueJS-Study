<template>
  <div>
    <Greet_Things/>
  </div>
</template>

<script>
import Greet_Things from './Greet.vue'
export default {
  name: 'App',
  components: {
    Greet_Things
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
