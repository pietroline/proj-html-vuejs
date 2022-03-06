<template>
    <div class="container-fluid d-flex justify-content-center align-items-center"> 
        <div class="row">
            <div class="col d-flex justify-content-center">
                <div class="text-center w-75">
                    <h4 class="ms_textStyle">Hello, I'am Martin</h4> 
                    <h4>Artist Coaching and Mentoring Might Be for you.</h4>
                    <MyBtn class="mt-4" :text="'Get started today'"/>
                </div>
                
            </div>
        </div>   
    </div>
</template>

<script>

    import MyBtn from "./partials/MyBtn.vue"

    export default {
        name: "MyJumbotron",
        components:{
            MyBtn,
        }
    }
</script>

<style lang="scss" scoped>

    @import "./../assets/variables";

    .container-fluid{
        height: 45rem;
        background-image: url("./../assets/img/jumbotron.png");
        background-size: cover;

        .ms_textStyle{
            font-family: "Comforter";
            color: $colorMartin;
            font-size: 3rem;
        }

    }
</style>