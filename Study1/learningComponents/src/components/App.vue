<template>
  <div>
    <Greet_Things name="Shezan" channelName="IIT" />
    <Greet_Things name="Mahmud" channelName="IIT" />
    <Greet_Things :name="name" :channelName="channel" />
  </div>
</template>

<script>
import Greet_Things from './Greet.vue'
export default {
  name: 'App',
  components: {
    Greet_Things
  },
  data() {
    return {
      name: 'Shezan',
      channel: 'iit'
    }
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
