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
        {text:'学习 JS',id:'1'},
        {text:'学习 Vue',id:'2'},
        {text:'学习 React',id:'3'},
        {text:'学习 Angular',id:'4'}
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
