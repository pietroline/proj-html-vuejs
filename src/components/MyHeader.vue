<template>
    <header class="container">
       <div class="row my-2">
           <div class="col-3 d-flex align-items-center justify-content-start">
               <LogoMaxCoach/>
               
           </div>     
           <div class="col-6 d-flex align-items-center justify-content-center">
               <MenuHeader :menuHeader="menuHeader"/>
               
            </div>
            <div class="col-3 d-flex align-items-center justify-content-end">
                <IconeSocialHeader/>
            </div>     
       </div>
    </header>
</template>

<script>

    import LogoMaxCoach from "./partials/LogoMaxCoach.vue";
    import MenuHeader from "./partials/MenuHeader.vue";
    import IconeSocialHeader from "./partials/IconeSocialHeader.vue";

    export default {
        name: "MyHeader",
        components:{
            LogoMaxCoach,
            MenuHeader,
            IconeSocialHeader,
        },
        props:{
            "menuHeader": Array,
        }
    }
</script>

<style>

</style>