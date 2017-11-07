<template>
  <div id="app">
    <img src="./assets/logo.png">
    <div id="ddd">dddd</div>
    <div id="NewNode">{{msg}}</div>
    <NewNode/>
    <HelloWorld/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import NewNode from './components/NewNode'
import Vue from 'vue'



export default {
  name: 'app',
  data(){
        return {
      
        }
  },

  components:{
    HelloWorld:HelloWorld,
    NewNode:NewNode
  },
   
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
