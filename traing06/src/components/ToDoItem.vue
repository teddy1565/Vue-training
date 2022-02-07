<template>
    <div>
        <input type="checkbox" :id="id" :checked="isDone" />
        <label :for="id">{{label}}</label>
    </div>
</template>
<script>
import uniqueId from "lodash.uniqueid";

export default {
    name:"ToDoItem",
    components: {
        ToDoItem
    },
    data() {
        return {
            ToDoItems: [
                {
                    id:uniqueId("todo-"),
                    label: "Learn Vue",
                    done: false
                },
                {
                    id:uniqueId("todo-"),
                    label: "Create a Vue project with the CLI",
                    done:true
                },
                {
                    id:uniqueId("todo-"),
                    label: "Have fun",
                    done:true
                },
                {
                    id:uniqueId("todo-"),
                    label: "Create a to-do list",
                    done:false
                }
            ]
        }
    }
}
</script>