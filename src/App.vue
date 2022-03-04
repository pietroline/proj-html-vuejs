<template>
  <div id="app">
    
    <MyHeader :menuHeader="menuHeader"/>
    <MyJumbotron/>
    <MySection1/>
    <MySection2/>
    <MySection3/>
    <MySection4/>
    <MySection6/>
    <MyFooter :menuFooter="menuFooter" />

  </div>
</template>

<script>

  import MyHeader from "./components/MyHeader.vue";
  import MyJumbotron from "./components/MyJumbotron.vue";
  import MySection1 from "./components/MySection1.vue";
  import MySection2 from "./components/MySection2.vue";
  import MySection3 from "./components/MySection3.vue";
  import MySection4 from "./components/MySection4.vue";
  import MySection6 from "./components/MySection6.vue";
  import MyFooter from "./components/MyFooter.vue";

  export default {
    name: 'App',
    components: {
      MyHeader,
      MyJumbotron,
      MySection1,
      MySection2,
      MySection3,
      MySection4,
      MySection6,
      MyFooter,
    },
    data(){
      return{
        menuHeader: ["Home", "Pages", "Courses", "Features", "Blog", "Shop"],
        menuFooter: {
          address: {
            mainTitle: "Address",
            menuTitle: ["382 NE 191st St # 87394 Miami, FL 33179-3899", "+1(305) 547-9909 (9am - 5pm EST, Monday - Friday)", "support@maxcoach.com"],
            menuIcon: ["bi bi-facebook", "bi bi-twitter", "bi bi-instagram", "bi bi-linkedin"],
            menuImg: null,
          },
          explore: {
            mainTitle: "Explore",
            menuTitle: ["Start here", "Success story", "Blog", "Courses", "Contact us"],
            menuIcon: null,
            menuImg: null,
          },
          information: {
            mainTitle: "Information",
            menuTitle: ["Membership", "Purchase guide", "Privacy policy", "Teams of services"],
            menuIcon: null,
            menuImg: null,
          },
          instagram: {
            mainTitle: {"social":"Instagram", "linkSocial":"@maxcoach"},
            menuTitle: null,
            menuIcon: null,
            menuImg: ["instagram1", "instagram2", "instagram3"], 
          },
        }
      }
    }
  }

</script>

<style lang="scss">
  
</style>
