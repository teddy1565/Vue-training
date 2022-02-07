<template>
    <div>
        <form @submit.prevent="onSubmit">
            <label for="new-todo-input">
                What needs to be done?
            </label>
            <input type="text" id="new-todo-input" name="new-todo" autocomplete="off" v-model="label">
            <button type="submit">Add</button>
        </form>
    </div>
</template>

<script>
export default {
    methods: {
        onSubmit() {
            if (this.label === "") {
                return false;
            }
            this.$emit("todo-added",this.label);
            // console.log("form submitted",this.label);
        }
    },
    data() {
        return {
            label:""
        };
    }
};
</script>