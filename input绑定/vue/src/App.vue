<template>
  <div id="app">
   <div class="appBox">
   我是父组件
   <p>
     <!-- {{str}} -->
<ul>
  <li v-show="item.flag" v-for="(item,index) in str" :key="index">
     <input :checked="item.flag" type="checkbox">
            {{item.title}}
  </li>
</ul>
   </p>
   </div>
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <HelloWorld @send=" acceptMsg"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'app',
  components: {
    HelloWorld
  },
  data(){
return {
  // str:""
  str:[]
}
  },
  methods:{
  acceptMsg(data){
    this.str=data,
console.log(data)
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
.appBox{
 width:100%;
 height:200px;
 
 background: orange
}
</style>
