<template>
  <div>
    <h2 v-if="num === 0"> The number is zero </h2>
    <h2 v-else-if="num < 0"> The number is negative </h2>
    <h2 v-else-if="num > 0"> The number is positive </h2>
    <h2 v-else> Not a number </h2>
    <div v-if="display">
      <h2> Shezan </h2>
      <h2> IIT </h2>
      <h2> Vue </h2>
    </div>
    <h2 v-if="showElement"> Using v-show </h2>
    <h2 v-show="showElement"> Using v-if </h2>

    <h2 v-for="(name, index) in names" :key="name"> {{index}} {{name}} </h2>
    <h2 v-for="name in fullNames" :key="name.first"> {{name.first}} {{name.last}} </h2>
    <div v-for="actor in actors" :key="actor.name">
      <h2>{{actor.name}}</h2>
      <h3 v-for="movie in actor.movies" :key="movie">{{movie}}</h3>
    </div>

    <h2 v-for="value in myInfo" :key="value">{{value}}</h2>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      num: 7,
      display: true,
      showElement: true,
      names: ['A', 'B', 'C'],
      fullNames: [
        {first: 'A1', last: 'A2'},
        {first: 'B1', last: 'B2'},
        {first: 'C1', last: 'C2'}
      ],
      actors: [
        {
          name: 'Christian Bale',
          movies: ['Batman', 'The Prestige']
        },
        {
          name: 'Di Caprio',
          movies: ['Titanic', 'Inception']
        }
      ],
      myInfo: {
        name: 'Shezan',
        channel: 'IIT',
        course: 'Vue 2'
      }
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
