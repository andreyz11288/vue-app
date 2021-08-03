<template>
  <div id="app">
    <h1>{{title}}</h1>
   <Button  @click="increments">Click me</Button>
   <DirectiveTest/>
   <StarRating :rating="4.5"/>
  </div>
</template>

<script>

import Button from "./components/Button";
import DirectiveTest from "./components/DirectivesTest.vue";
import StarRating from "./components/StarRating.vue";

export default {
  name: 'App',
  components: {
    Button,
    DirectiveTest,
    StarRating
  },
  data(){
    return{
      amountOfClicks: 0
    }
  },
  computed:{
   title(){
     return ` Amount of click ${this.amountOfClicks}`
   }
  },
  methods:{
    increments(){
      this.amountOfClicks += 1
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
