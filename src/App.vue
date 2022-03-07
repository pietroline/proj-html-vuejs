<template>
  <div id="app">
    
    <MyHeader :menuHeader="jsonData.menuHeader.menu" :icons="jsonData.menuHeader.icons"/>
    <MyJumbotron/>
    <ArtgtCoaching1 :title="jsonData.sectionArtigtCoaching.title" :subTitles="jsonData.sectionArtigtCoaching.subTitles" :data="jsonData.sectionArtigtCoaching.contents.helpYou"/>
    <ArtgtCoaching2 :goal="jsonData.sectionArtigtCoaching.contents.goal"/>
    <ArtgtCoaching3 :video="jsonData.sectionArtigtCoaching.contents.video"/>
    <UsersTestimonials :data="jsonData.sectionTestimonials"/>
    <ArtistCoaching :data="jsonData.sectionArtistCoaching"/>
    <ArticleAndTips :title="jsonData.articleAndTips.title" :subTitles="jsonData.articleAndTips.subTitles" :data="jsonData.articleAndTips.contents"/>
    <UpcomingEvent :data="jsonData.sectionUpcomingEvents"/>
    <MyFooter :menuFooter="jsonData.menuFooter" />

  </div>
</template>

<script>

  import data from "./data.json"

  import MyHeader from "./components/MyHeader.vue";
  import MyJumbotron from "./components/MyJumbotron.vue";
  import ArtgtCoaching1 from "./components/ArtgtCoaching1.vue";
  import ArtgtCoaching2 from "./components/ArtgtCoaching2.vue";
  import ArtgtCoaching3 from "./components/ArtgtCoaching3.vue";
  import UsersTestimonials from "./components/UsersTestimonials.vue";
  import ArtistCoaching from "./components/ArtistCoaching.vue";
  import ArticleAndTips from "./components/ArticleAndTips.vue";
  import UpcomingEvent from "./components/UpcomingEvent.vue";
  import MyFooter from "./components/MyFooter.vue";

  export default {
    name: 'App',
    components: {
      MyHeader,
      MyJumbotron,
      ArtgtCoaching1,
      ArtgtCoaching2,
      ArtgtCoaching3,
      UsersTestimonials,
      ArtistCoaching,
      ArticleAndTips,
      UpcomingEvent,
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
