<template>
  <!-- <div id="app"> -->
  <div>
    <div>
      {{greet}} {{name}}
    </div>
    <div v-text="channel1"></div>
    <div v-html="channel2"></div>
    <h2 v-bind:id="h_id"> Headinggg </h2>
    <button :disable="isDisabled"> Butttooooonnn </button>
    <h2 class="underlineClass"> Underline teeeexttttt </h2>
    <h2 :class='status'> Staaatusss </h2>
    <h2 :class="isPromoted && 'promotedClass'"> Promoted Movieeeee </h2>
    <h2 :class="isSold ? 'sold' : 'new' "> Movieeeeeeeeee </h2>
    <h2 :class="['new', 'promotedClass']"> Newly promoted movie </h2>
    <h2 :class="[isPromoted && 'promotedClass', isSold ? 'new' : 'sold']"> Array conditional movie </h2>
    <h2 :class="{
      promotedClass: isPromoted,
      new: isSold,
      sold: !isSold
    }"> Object conditional movie </h2>
    <h2 :style="{
      color: highlightColor,
      fontSize: headerSize + 'px',
      padding: '20px'
    }"> Inline Style </h2>
    <h2 :style="headerStyleObject"> Style Object </h2>
    <h2 :style="[baseStyleObject, successStyleObject]"> Success Style </h2>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  // components: {
  //   HelloWorld
  // }
  data() {
    return {
      greet: "Hellooooo",
      name: "Shezan",
      channel1: 'IIT',
      channel2: '<b>IIT</b>',
      h_id: 'Heading',
      isDisabled: true,
      status: 'success',
      isPromoted: true,
      isSold: false,
      highlightColor: 'orange',
      headerSize: 50,
      headerStyleObject: {
        color: 'Royal blue',
        fontSize: '50px',
        padding: '20px'
      },
      baseStyleObject: {
        fontSize: '50px',
        padding: '10px'
      },
      successStyleObject: {
        color: 'green',
        backgroundColor: 'lightgreen',
        border: '1 px solid green'
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
#Heading {
  font-size: 50px;
  color: blue
}
.underlineClass {
  text-decoration: underline;
}
.promotedClass {
  font-style: italic;
}
.new {
  color: green
}
.sold {
  color: red;
}
</style>
