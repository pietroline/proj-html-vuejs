<template>
  <div>
      <a href="#" 
        v-for="(icon, index) in icons" 
        :key="'icons header' + index">

        <!-- inizio contenuto a -->
        <i :class="icon"></i>
        <!-- fine contenuto a -->
        </a>
      
  </div>
</template>

<script>
    export default {
        name: "IconeSocialHeader",
        props:{
            "icons": Array,
        }
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