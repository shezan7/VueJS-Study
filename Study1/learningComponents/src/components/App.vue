<template>
  <div>
    <Greet_Things name="Shezan" channelName="IIT" />
    <Greet_Things name="Mahmud" channelName="IIT" />
    <Greet_Things :name="name" :channelName="channel" />
    
    <Article_Things title="Article Title" :likes="50" :isPublished="true" />

    <Component_C />

    <button @click="showPopup = true">Show PopUp</button>
    <Pop_Up v-show="showPopup" @close="showPopup = false" />

    <Input_Things v-model="i_name" />
  </div>
</template>

<script>
import Greet_Things from './Greet.vue'
import Article_Things from './Article.vue'
import Component_C from './ComponentC.vue'
import Pop_Up from './PopUp.vue'
import Input_Things from './Input.vue'
export default {
  name: 'App',
  components: {
    Greet_Things,
    Article_Things,
    Component_C,
    Pop_Up,
    Input_Things
},
  data() {
    return {
      name: 'Shezan',
      channel: 'iit',
      showPopup: false,
      i_name: ''
    }
  },
  provide: {
    username: 'Shezan'
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
