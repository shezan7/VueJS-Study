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

    <CardComponent>Card Content</CardComponent>
    <CardComponent>
      <h2>Card Content</h2>
    </CardComponent>
    <CardComponent>
      <img src="https://machinelearningmastery.com/wp-content/uploads/2016/09/icon-150x150.png" alt="">
    </CardComponent>

    <CardComponent>
      <template v-slot:header>
        <h3>Header</h3>
      </template>
      <template v-slot:default>
        <img src="https://machinelearningmastery.com/wp-content/uploads/2016/09/icon-150x150.png" alt="">
      </template>
      <template v-slot:footer>
        <button>View Details</button>
      </template>
    </CardComponent>

    <NameList>
      <template v-slot:default="slotProps">
        {{slotProps.firstName}} {{slotProps.lastName}}
      </template>
    </NameList>
    <NameList>
      <template v-slot:default="slotProps">
        {{slotProps.lastName}}, {{slotProps.firstName}}
      </template>
    </NameList>
    <NameList>
      <template v-slot:default="slotProps">
        {{slotProps.firstName}}
      </template>
    </NameList>

    <h5>Parent Component</h5>
    <ChildStyles>
      <h5>Child Component</h5>
    </ChildStyles>

    <button @click="activeTab = 'TabA'"> Tab A</button>
    <button @click="activeTab = 'TabB'"> Tab B</button>
    <button @click="activeTab = 'TabC'"> Tab C</button>
    <!-- <TabA v-if="activeTab === 'TabA'" />
    <TabB v-if="activeTab === 'TabB'" />
    <TabC v-if="activeTab === 'TabC'" /> -->
    <!-- <component :is="activeTab" /> -->
    <keep-alive>
      <component :is="activeTab" />
    </keep-alive>

  </div>
</template>

<script>
import Greet_Things from './Greet.vue'
import Article_Things from './Article.vue'
import Component_C from './ComponentC.vue'
import Pop_Up from './PopUp.vue'
import Input_Things from './Input.vue'
import CardComponent from './Card.vue'
import NameList from './NameList.vue'
import ChildStyles from './ChildStyles.vue'
import TabA from './TabA.vue'
import TabB from './TabB.vue'
import TabC from './TabC.vue'

export default {
  name: 'App',
  components: {
    Greet_Things,
    Article_Things,
    Component_C,
    Pop_Up,
    Input_Things,
    CardComponent,
    NameList,
    ChildStyles,
    TabA,
    TabB,
    TabC
  },
  data() {
    return {
      name: 'Shezan',
      channel: 'iit',
      showPopup: false,
      i_name: '',
      activeTab: ''
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

h5 {
  color: red;
}
</style>
