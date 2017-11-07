<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <div id='uu'>uuuu</div>
    <h2>Essential Links</h2>
  </div>
</template>



<script>
import Vue from 'vue'

export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: '欢迎'
    }
  },
  created(){
   
  },
  mounted(){
    //  let ii=0;
    // for(let key in this){
    //   console.log(++ii);
    //   console.log(key)
    // }
    let v = new Vue({
      el:'#uu'
    })
    //alert(v);
    v.$el.hidden= true;
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
