<template>
    <section>
        <div class="opacity-25">
            <div class="ms_line"></div>
            <div class="ms_circleWave"/>
            <div class="ms_shape1"/>
            <div class="ms_shape2"/>
        </div>

        <div class="container">
            
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

    section{
            position: relative;

        & .ms_line{
            background-image: url("./../assets/img/maxcoach-shape-line-background.png");
            background-size: contain;
            background-repeat: no-repeat;

            height: 100vw;
            width: 100vw;

            position: absolute;
            top: -4rem;
            right: 0;
        }

        & .ms_circleWave{
            background-image: url("./../assets/img/maxcoach-shape-circle-wave.png");
            background-size: contain;
            background-repeat: no-repeat;

            height: 10rem;
            width: 10rem;

            position: absolute;
            top: 8rem;
            right: -4rem;
        }

        & .ms_shape1{
            background-image: url("./../assets/img/maxcoach-shape-01.png");
            background-size: contain;
            background-repeat: no-repeat;
            transform: rotate(230deg);

            height: 20rem;
            width: 20rem;

            position: absolute;
            top: -2rem;
            left: -5rem;
        }

        & .ms_shape2{
            background-image: url("./../assets/img/maxcoach-shape-02.png");
            background-size: contain;
            background-repeat: no-repeat;

            height: 30rem;
            width: 30rem;

            position: absolute;
            top: 2rem;
            left: 75rem;

        }
        
    }

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