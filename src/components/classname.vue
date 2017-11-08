<template>
  <div id="app">
	hello，{{msg}}
  <a v-bind:href="url">百度</a>
  	<div v-html="rawHtml"></div>
    <img :src='src'>
    <div :class="cc">gg</div>
  	<input type="button" @click='changeText' value='改纯文本'/>
    <input type="button" @click='changeHtml' value='改html'/>
    <input type="button" @click='changeImg' value='改图'/>
    <input type="button" @click='changeClass' value='改Class'/>
  </div>
 </template>	
  <script>
  	export default{
  		data(){
  			return {
  				msg:'张三',
  				rawHtml:"<font size='25' color='green'>世界</font>",
          url:'http://www.baidu.com',
          src:'http://5b0988e595225.cdn.sohucs.com/images/20170913/f72b4d60fa8b4149bc1d3e723b3368f7.jpeg',
          cc:{wh:true,c1:true},
  			}
  		},
  		methods:{
  			changeText:function(){
  				this.msg='李四';
  			},
        changeHtml:function(){
          this.rawHtml='<b>天气雾霾</br>';
        },
        changeImg:function(){
        this.src='http://www.qcyx123.com/UploadFile/news/2017/0914/2017091410343792296600.jpg?imageView&thumbnail=550x0'        
        },
        changeClass:function(){
          this.cc={wh:true,c2:true}


        }
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