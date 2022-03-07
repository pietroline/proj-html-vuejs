<template>
  <section class="container-fluid">

        <!-- inizio background-image -->
        <div class="row">
            
            
            
            
            <div class="ms_wave"/>
        </div>
        <!-- fine background-image -->

        <div class="row row-cols-1">
            <div class="col text-center position-relative">
                <div class="ms_video_overlay position-relative d-inline-block">
                    <img class="ms_video" src="./../assets/img/artist-video-poster.jpg" alt="artist-video-poster">
                    <a href="#">
                        <img class="position-absolute top-50 start-50 translate-middle" src="./../assets/img/icon-youtube-play.png" alt="icon-youtube-play">
                    </a>
                </div>

                <div class="ms_shape3"/>
                <div class="ms_shape4"/>
                <div class="ms_shape5"/>
                <div class="ms_ring"/>
                 
            </div>
        </div>
  </section>
  
</template>

<script>
    export default {
        name: "MyProva"
    }
</script>

<style lang="scss" scoped>

section{
        position: relative;

        .ms_video_overlay{
            cursor: pointer;
            display: inline;



            .ms_video{
                opacity: 100%;
                transition: opacity 2s;
            }

            &:hover .ms_video{
                opacity: 60%;
            }


            & img{
                position: relative;
                z-index: 5;
            }


            & a img{
                width: 5rem;
                transition: width 1s; 
            }

            &:hover a img{
                width: 10rem;
                opacity: 80%;

                &:hover{
                    opacity: 100%;
                }
            }



        }


        & .ms_shape3{
            background-image: url("./../assets/img/maxcoach-shape-03.png");
            background-size: contain;
            background-repeat: no-repeat;

            height: 15rem;
            width: 15rem;

            position: absolute;
            top: -5rem;
            left: 12rem;

        }

        & .ms_shape4{
            background-image: url("./../assets/img/maxcoach-shape-04.png");
            background-size: contain;
            background-repeat: no-repeat;

            height: 8rem;
            width: 8rem;

            position: absolute;
            top: -2rem;
            left: 15rem;


        }

        & .ms_shape5{
            background-image: url("./../assets/img/maxcoach-shape-05.png");
            background-size: contain;
            background-repeat: no-repeat;

            height: 8rem;
            width: 8rem;

            position: absolute;
            bottom: -1rem;
            right: 15rem;

        }

        & .ms_ring{
            background-image: url("./../assets/img/maxcoach-shape-ring.png");
            background-size: contain;
            background-repeat: no-repeat;

            height: 8rem;
            width: 8rem;

            position: absolute;
            top: 8rem;
            right: 14rem;;

            z-index: 6;
        }

        & .ms_wave{
            background-image: url("./../assets/img/wave.png");
            background-size: cover;
            background-repeat: no-repeat;

            height: 30rem;
            width: 100vw;

            position: absolute;
            bottom: 0;
            

        }
          
    }

</style>