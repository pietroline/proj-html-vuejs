<template>
  <div id="app">
    
    <MyHeader :menuHeader="menuHeader"/>
    <MyJumbotron/>
    <MyFooter :menuFooter="menuFooter" />

  </div>
</template>

<script>

  import MyHeader from "./components/MyHeader.vue";
  import MyJumbotron from "./components/MyJumbotron.vue";
  import MyFooter from "./components/MyFooter.vue";

  export default {
    name: 'App',
    components: {
      MyHeader,
      MyJumbotron,
      MyFooter,
    },
    data(){
      return{
        menuHeader: ["Home", "Pages", "Courses", "Features", "Blog", "Shop"],
        menuFooter: {
          address: {
            mainTitle: "Address",
            menuTitle: ["382 NE 191st St # 87394 Miami, FL 33179-3899", "+1(305) 547-9909 (9am - 5pm EST, Monday - Friday)", "support@maxcoach.com"],
            menuImg: null,
          },
          explore: {
            mainTitle: "Explore",
            menuTitle: ["Start here", "Success story", "Blog", "Courses", "Contact us"],
            menuImg: null,
          },
          information: {
            mainTitle: "Information",
            menuTitle: ["Membership", "Purchase guide", "Privacy policy", "Teams of services"],
            menuImg: null,
          },
          instagram: {
            mainTitle: {"social":"Instagram", "linkSocial":"@maxcoach"},
            menuTitle: null,
            menuImg: ["instagram1.jpeg", "instagram2.jpg", "instagram3.jpg"], 
          },
        }
      }
    }
  }

</script>

<style lang="scss">

</style>
