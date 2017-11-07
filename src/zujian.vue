<template>
  <div id="app">
    <img src="./assets/logo.png">
    <div id="ddd">dddd</div>
    <myComp/><myComp/><myComp/>
    <button @click='gohome'>Home</button>      
    <button @click='post'>Posts</button>      
    <button @click='active'>Archive</button> 
    <component :is="currentView"></component>
    <HelloWorld/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import NewNode from './components/NewNode'
import Vue from 'vue'

var myComponent = Vue.extend({
    //用预定义选项来创建可复用组件的构造器
  template:'<div>This is my first a 组件!</div>',
      components:{
        // abc:HelloWorld //嵌套组件（父子组件）
      }
})

let aa = new Vue({
  template:'<div>hello,我是aa</div>'
})


Vue.component('myComp',myComponent)  //全局组件



let components = {
  home:Vue.extend({
      template:'<div>home 组件!</div>',

  }),

  post:Vue.extend({
        template:'<div>post 组件!</div>',

  }),

  active:NewNode
}

//组件与实例的区别：实例能够操作东西，组件没法直接用户，组件是虚拟DOM的模板，new出来之后就是一个虚拟化实例


export default {
  name: 'app',
  data(){
    return{
      currentView:components.home
    }
  },
  components:{
    HelloWorld:HelloWorld,
    //myComp:myComponent  //局部注册
  },
  mounted(){
    // let dd = new Vue({
    //   el:'#ddd'

    // });
  //aa.$mount(dd.$el);
  //new myComponent().$mount(dd.$el);
  },
  methods:{
    gohome:function(){
      this.currentView = components.home
    },
    post:function(){
      this.currentView = components.post

    },
    active:function(){
      this.currentView = components.active

    }
  }



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
