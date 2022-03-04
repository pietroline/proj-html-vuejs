<template>
  <section class="my-2">
        <span>Start TOMORROW! Our biggerest event of the year...</span>
        <span class="mx-3 text-dark">
            <i class="bi bi-clock me-2"></i>
            <span>00:00:00:00</span>
        </span>
        <button class="btn px-4 py-2">Get ticket</button>
  </section>
</template>

<script>
    export default {
        name: "BiggestEvent",
    }
</script>

<style lang="scss" scoped>

    @import "./../../assets/variables.scss";

    .btn{
        background-color: $orange;
        color: #fff;
        font-weight: bold;

        &:hover{
            background-color: $iceCold;
        }
    }

    
</style>