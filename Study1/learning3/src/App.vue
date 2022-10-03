<template>
  <div>
    <h2> Add Method - {{add(2,3,5)}} </h2>
    <h2> Add Method - {{add(10,15,20)}} </h2>
    <h2> Multiply Method - {{multiply(10)}} </h2>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      baseMultiplier: 5
    }
  },
  methods: {
    add(a,b,c) {
      return a+b+c
    },
    multiply(num) {
      return num*this.baseMultiplier
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
