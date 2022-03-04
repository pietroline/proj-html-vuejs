<template>
    <section class="container">
        <div class="row">
            <div class="col text-center">
                <h4 class="ms_textStyle">Artigt coaching</h4>
                <h4 class="fs-2">I understand what it takes to create.</h4>
                <h4 class="fs-2">I can help you whith</h4>
            </div>
        </div>
        <div class="row">
            <div class="col">
                <div class="ms_contenitoreImg my-3">
                    <img src="./../assets/img/artist-box-image-01.png" alt="artist-box-image-01">
                </div>
                <h5 class="fs-5">Online Coures</h5>
                <p class="ms_text">Online art coaching now offers you a very powerful way to redesign your artist mind.</p>
            </div>
            <div class="col">
                <div class="ms_contenitoreImg my-3">
                    <img src="./../assets/img/artist-box-image-02.png" alt="artist-box-image-02">
                </div>
                <h5 class="fs-5">One to One</h5>
                <p class="ms_text">Getting the necessary clarity about the current state to help you improve your ability.</p>
            </div>
            <div class="col">
                <div class="ms_contenitoreImg my-3">
                    <img src="./../assets/img/artist-box-image-03.png" alt="artist-box-image-03">
                </div>
                <h5 class="fs-5">Anywhere</h5>
                <p class="ms_text">Access to valuable and portable program which allow you to setup and live anywhere you want.</p>
            </div>
            <div class="col">
                <div class="ms_contenitoreImg my-3">
                    <img src="./../assets/img/artist-box-image-04.png" alt="artist-box-image-04">
                </div>
                <h5 class="fs-5">On Time</h5>
                <p class="ms_text">Punctually is our top priority bacause it's an essential criteria to assess a program quality.</p>
            </div>
             
        </div>
        
    </section>
</template>

<script>
    export default {
        name: "MySection1",
    }
</script>

<style lang="scss" scoped>

    @import "./../assets/variables.scss";

    .container{

        margin: 5rem auto;

        .ms_textStyle{
            font-family: "Comforter";
            color: $colorMartin;
            font-size: 3rem;
        }

        .ms_contenitoreImg{
            width: 8rem;
            height: 8rem;
            

            img{
                width: 100%;
            }
        }

        p.ms_text{
            color: $boulder;
        }
    }

</style>