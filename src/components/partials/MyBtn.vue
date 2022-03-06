<template>
    <button class="btn px-4 py-2" :class="type=='dark'?'dark':'light'">
        {{text}}
         <i v-if="bootstrapIcon != null" :class="bootstrapIcon"></i>
    </button>
</template>

<script>
    export default {
        name: "MyBtn",
        props:{
            "text": String,
            "bootstrapIcon": String,
            "type": String,
        }
    }
</script>

<style lang="scss" scoped>

    @import "./../../assets/variables.scss";

    .dark{
        background-color: $orange;
        color: $white;
        font-weight: bold;

        &:hover{
            background-color: $iceCold;
            color: $white;
        }
    }

    .light{
        background-color: $bisque;
        color: $orange;
        font-weight: bold;
       
        &:hover{
            background-color: $iceCold;
            color: $white;
        }
    }

</style>