<template>
  <div id="app">
    <h1>{{title}}</h1>
    <h1 v-text="title"></h1>
    <h1 v-html="title"></h1>
    <input type="text" v-model="newItem" v-on:keyup.enter="addNew">
    <ul>
        <li v-for="item in items" v-bind:class="{finished:item.isFinished}" v-on:click="toggleFinish(item)">
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
      ],
      newItem:''
    }
  },
  methods:{
    toggleFinish:function(item){
      // console.log(item);
      item.isFinished=!item.isFinished;
    },
    addNew:function(){
      // this.newItem;
      // console.log(this.newItem);
      this.items.push({
        label:this.newItem,
        isFinished:false
      })
      this.newItem='';
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
