<template>
  <div>
      <a href="#"><i class="bi bi-twitter mx-2"></i></a>
      <a href="#"><i class="bi bi-facebook mx-2"></i></a>
      <a href="#"><i class="bi bi-instagram mx-2"></i></a>
      <a href="#"><i class="bi bi-linkedin mx-2"></i></a>
  </div>
</template>

<script>
    export default {
        name: "IconeSocialHeader",
    }
</script>

<style lang="scss" scoped>

    @import "./../../assets/variables.scss";
    
    .bi{
        color: $boulder;
    }

    a:hover i{
        color: $silver;
    }

</style>