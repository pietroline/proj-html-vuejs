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
                    <h4 class="ms_textStyle">{{data.title}}</h4>
                    <h4 class="fs-2" 
                        v-for="(subTitle, index) in data.subTitles" 
                        :key="'subtitle '+index">

                    <!-- inizio contenuto h4 -->
                    {{subTitle}}
                    <!-- fine contenuto h4 -->

                    </h4>
                    
                </div>
            </div>
            
            <div class="row">

                <div class="col" v-for="(content, index) in data.contents" :key="'Artigt coaching '+index">
                    <div class="ms_contenitoreImg my-3">
                        <img :src="require(`./../assets/img/${content.image}.png`)" :alt="content.image">
                    </div>
                    <h5 class="fs-5">{{content.texts.title}}</h5>
                    <p class="ms_text">{{content.texts.paragraph}}</p>
                </div>
               
            </div>

        </div>
    </section>
</template>

<script>
    export default {
        name: "MySection1",
        props:{
            "data": Object,
        }
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