<template>
  <div id="app">
    <hello-world v-for="todo in todos" :key="todo.id" :msg="todo.text" :deal="addList"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  data(){
    return {
      msg:'Welcome to Your Vue.js App',
      todos:[
        {text:'学习1 JS',id:'2'},
        {text:'学习2 Vue',id:'3'},
        {text:'学习3 React',id:'4'},
        {text:'学习4React',id:'9'},
        {text:'学习4React',id:'9'},
      ]
    } 
  },
  methods:{
    addList:function(item){
      console.log(item)
      this.todos.push(item)
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
