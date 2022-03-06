<template>
    <button class="btn px-4 py-2">{{text}}</button>
</template>

<script>
    export default {
        name: "MyBtn",
        props:{
            "text": String,
        }
    }
</script>

<style lang="scss" scoped>

    @import "./../../assets/variables.scss";

    .btn{
        background-color: $orange;
        color: $white;
        font-weight: bold;

        &:hover{
            background-color: $iceCold;
        }
    }

</style>