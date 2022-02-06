<template>
    <div>
        <input type="checkbox" id="todo-item" checked="false" />
        <label for="todo-item">{{label}}</label>
    </div>
</template>

<script>
export default {
    name:"RegisTeringProps",
    props:{
        label:{ required:true, type:String},
        done: { default: false, type:Boolean}
    },
    data() {
        console.log(this.done)
        return {
            isDone: this.done
        };
    }
};
</script>