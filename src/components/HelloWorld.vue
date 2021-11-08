<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <button @click="dealAddAction" >
      add
    </button>
    <input type="text" v-model="data1" name="" id="">
  </div>
  
</template>

<script>
export default {
  name: 'HelloWorld',
  props: ['msg','deal'],
  data(){
    return {
      test:'testing',
      id:'4',
      data1:''
    }
  },
  methods:{
    dealAddAction:function(){
      console.log('1')
      this.$emit('deal',{text:'add',id:++this.id})
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
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
