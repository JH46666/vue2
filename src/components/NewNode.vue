<template>
  <div id="app">
	hello，{{msg}}
  	 <h1>{{msg.split('').join(',')}}</h1>
     <span>{{ number+1 }}</span> 
     <span>{{ok ? 'YES' : 'NO'}}</span> 
    <div v-if="show">进入if</div> 
    <div v-else>进入else</div>
    <input type="button" @click='changeClass' value='改Class'/>
  </div>
 </template>	
  <script>
  	export default{
  		data(){
  			return {
  				msg:'abcde',
          number:15,
          ok:true,
          show:true,

  			}
  		},
  		methods:{
  	
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

.wh{
  width: 400px;
  height: 200px;
}
.c1{
  border: 2px solid yellow
}
.c2{
  width: 50px;
  height: 50px;

}
</style>






















































</template>