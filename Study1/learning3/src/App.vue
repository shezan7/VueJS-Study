<template>
  <div>
    <h2> Add Method - {{add(2,3,5)}} </h2>
    <h2> Add Method - {{add(10,15,20)}} </h2>
    <h2> Multiply Method - {{multiply(10)}} </h2>

    <div>
      <h2> {{name}} </h2>
      <div>
        <button @click="changeName">Change Name</button>
      </div>
    </div>

    <div>
      <div>
        <h2 v-if="name2===true" class="divChange"> Shezan Al-Mahmud updated </h2>
        <h2 v-else class="divChange2"> Shezan Al-Mahmud </h2>
      </div>
      <div>
        <button @click="changeDiv">Change Div</button>
      </div>
    </div>

  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      baseMultiplier: 5,
      name: 'Shezan',
      name2: false
    }
  },
  methods: {
    add(a,b,c) {
      return a+b+c
    },
    multiply(num) {
      return num*this.baseMultiplier
    },
    changeName() {
      this.name = 'Al-Mahmud'
    },
    changeDiv() {
      this.name2 = true
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
.divChange {
  color: red;
  font-size: 50px;
}
.divChange2 {
  color: blue
}
</style>
