<template>
  <div id="app">
    
    <MyHeader :menuHeader="jsonData.menuHeader.menu" :icons="jsonData.menuHeader.icons"/>
    <MyJumbotron/>
    <MySection1 :data="jsonData.sectionArtigtCoaching"/>
    <MySection2/>
    <MySection3/>
    <MySection4/>
    <MySection5/>
    <MySection6/>
    <MyFooter :menuFooter="jsonData.menuFooter" />

  </div>
</template>

<script>

  import data from "./data.json"

  import MyHeader from "./components/MyHeader.vue";
  import MyJumbotron from "./components/MyJumbotron.vue";
  import MySection1 from "./components/MySection1.vue";
  import MySection2 from "./components/MySection2.vue";
  import MySection3 from "./components/MySection3.vue";
  import MySection4 from "./components/MySection4.vue";
  import MySection5 from "./components/MySection5.vue";
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
      MySection5,
      MySection6,
      MyFooter,
    },
    data(){
      return{
        jsonData: data,
      }
    }
  }

</script>

<style>
  
</style>
