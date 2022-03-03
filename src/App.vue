<template>
  <div id="app">
    
    <MyHeader :menuHeader="menuHeader"/>
    <MyJumbotron/>
    
  </div>
</template>

<script>

  import MyHeader from "./components/MyHeader.vue";
  import MyJumbotron from "./components/MyJumbotron.vue";

  export default {
    name: 'App',
    components: {
      MyHeader,
      MyJumbotron,
    },
    data(){
      return{
        menuHeader: ["Home", "Pages", "Courses", "Features", "Blog", "Shop"]
      }
    }
  }

</script>

<style lang="scss">

</style>
