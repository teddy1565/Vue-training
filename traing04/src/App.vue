<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <hr>
    <!--<ToDoItem/> equal <to-do-item> 使用大駝峰命名法-->
    <ToDoItem/>
    <to-do-item></to-do-item>
    <RegisTeringProps label="hello world" :done="true"/>
    <LodashUniquid label="LodashTest" :done="true"/>
    <LodashUniquid label="LodashTest2" :done="true"/>
    <LodashUniquid label="LodashTest3" :done="true"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

import ToDoItem from "./components/ToDoItem.vue"

import RegisTeringProps from "./components/RegisTeringProps.vue"

import LodashUniquid from "./components/LodashUniquid.vue"

export default {
  name: 'App',
  components: {
    HelloWorld,
    ToDoItem,
    RegisTeringProps,
    LodashUniquid
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
