<template>
  <div id="app">
    <h1>To-Do List</h1>
    <ToDoForm @todo-added="addToDo"/>
    <ul>
      <li v-for="item in ToDoItems" v-bind:key="item.id">
        <ToDoItem v-bind:label="item.label" v-bind:done="true" v-bind:id="item.id"/>
      </li>
    </ul>
  </div>
</template>

<script>

import ToDoItem from "./components/ToDoItem.vue";
import ToDoForm from "./components/ToDoForm.vue";
import uniqueId from "lodash.uniqueid";


export default {
  name: 'App',
  components: {
    ToDoItem,
    ToDoForm
  },
  data() {
    return {
      ToDoItems: [
        {
          id:uniqueId("todo-"),
          "label":"Learn Vue",
          done:false
        },
        {
          id:uniqueId("todo-"),
          "label":"Create a Vue project with the CLI",
          done:true
        },
        {
          id:uniqueId("todo-"),
          "label":"Have fun",
          done:true
        },
        {
          id:uniqueId("todo-"),
          "label":"Create a to-do list",
          done:false
        }
      ]
    };
  },
  methods: {
    addToDo(toDoLabel) {
      console.log(this);
      this.ToDoItems.push({
        id:uniqueId("todo-"),
        label:toDoLabel,
        done:false
      });
      console.log("To-do added:",toDoLabel);
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
