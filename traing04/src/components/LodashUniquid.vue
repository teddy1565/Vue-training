<template>
    <div>
        <input type="checkbox" id="todo-item" checked="false" />
        <label for="todo-item">{{label}}</label>
    </div>
</template>

<script>
    import uniqueId from 'lodash/uniqueId';
    export default {
        props: {
            label: {
                required: true,
                type:String
            },
            done: {
                default:false,
                type:Boolean
            }
        },
        data() {
            let id = uniqueId("todo-");
            console.log(id)
            return {
                isDone: this.done,
                id: id
            };
        }
    }
</script>