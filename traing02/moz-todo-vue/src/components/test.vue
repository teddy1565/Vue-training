<template>
    <div class="test">
        {{ msg }}
    </div>
</template>
<script>
    export default {
        name:"Test",
        props:{
            msg:String
        }
    }
</script>