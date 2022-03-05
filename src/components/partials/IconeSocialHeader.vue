<template>
  <div>
      <a href="#"><i class="bi bi-twitter"></i></a>
      <a href="#"><i class="fa-brands fa-facebook-f"></i></a>
      <a href="#"><i class="bi bi-instagram"></i></a>
      <a href="#"><i class="bi bi-linkedin"></i></a>
  </div>
</template>

<script>
    export default {
        name: "IconeSocialHeader",
    }
</script>

<style lang="scss" scoped>

    @import "./../../assets/variables.scss";
    
    a {
        color: $boulder;
        margin: 0 0.8rem;
    } 

    a:hover{
        color: $silver;
        
    }

</style>