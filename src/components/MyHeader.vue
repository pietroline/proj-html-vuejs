<template>
    <header class="container-fluid">

        <div id="ms_headerTop" class="row">
            <div class="col">
                <BiggestEvent/>
            </div>
        </div>

        <div id="headerBottom" class="container">
             <div class="row my-3">

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
        </div>
        
    </header>
</template>

<script>

    import BiggestEvent from "./partials/BiggestEvent.vue";
    import LogoMaxCoach from "./partials/LogoMaxCoach.vue";
    import MenuHeader from "./partials/MenuHeader.vue";
    import IconeSocialHeader from "./partials/IconeSocialHeader.vue";

    export default {
        name: "MyHeader",
        components:{
            BiggestEvent,
            LogoMaxCoach,
            MenuHeader,
            IconeSocialHeader,
        },
        props:{
            "menuHeader": Array,
        }
    }
</script>

<style lang="scss" scoped>
    
    @import "./../assets/variables.scss";

    header{
        background-color: $white;
        position: fixed;
        z-index: 999;

    }

    #ms_headerTop{
        background-color: $colorHeaderTop;
        color: $dustyGray;
    }
</style>