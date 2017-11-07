<template>
  <div id="app">
	hello，{{msg}}
  	<div v-html="rawHtml"></div>
  	<input type="button" @click='changeText' value='改纯文本'/>
  </div>
 </template>	
  <script>
  	export default{
  		data(){
  			return {
  				msg:'张三',
  				rawHtml:"<font size='25' color='green'>世界</font>"
  			}



  		},
  		methods:{
  			changeText:function(){
  				this.msg='李四',
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






















































</template>