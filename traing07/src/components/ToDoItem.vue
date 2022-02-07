<template>
    <div>
        <input type="checkbox" v-bind:checkked="isDone" v-bind:id="id"/>
        <label v-bind:for="id">{{label}}</label>
    </div>
</template>

<script>

export default {
    props:{
        label:{
            required:true,
            type:String
        },
        done:{
            default:false,
            type:Boolean
        },
        id: {
            required:true,
            type:String
        }
    },
    data() {
        return {
            isDone: this.done
        }
    }
};
</script>