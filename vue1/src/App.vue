<template>
<div id="app">
  <h1>{{title}}</h1>
  <FirstFile v-on:changeTitle="updateTitleText($event)"></FirstFile>
  </div>
  </template>
<script>
import FirstFile from './components/first-file.vue'
export default {
  name: 'App',
  components: {
    FirstFile
    },
    data(){
    return{
      title:" child to parent"
    }
  },
  methods:{
    updateTitleText(title)
    {
      this.title=title
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
