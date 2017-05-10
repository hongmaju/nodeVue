<template>
  <div id="app">
    <h1>{{title}}</h1>
    <h1 v-text="title"></h1>
    <h1 v-html="title"></h1>
    <ul>
        <li v-for="item in items" class="finished">
        {{item.label}}
        </li>
    </ul>
  </div>
</template>

<script>

export default {
  
   data () {
    return {
      title: '<span>?</span>this is a todolist',
      items:[
          {
            label:'coding',
            isFinished:false
  
          },
          {
            label:'walking',
            isFinished:true
  
          }
      ]
    }
  }
}
</script>

<style>
.finished{
  text-decoration:underline;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
