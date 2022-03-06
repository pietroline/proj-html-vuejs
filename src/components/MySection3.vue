<template>
    <section>
        <div class="container-fluid">
            
            <!-- inizio background-image -->
            <div class="row">
                <div class="ms_shape3"/>
                <div class="ms_shape4"/>
                <div class="ms_shape5"/>
                <div class="ms_ring"/>
                <div class="ms_wave"/>
            </div>

            <!-- fine background-image -->

            <div class="row row-cols-1">
                <div class="col text-center position-relative">
                <img src="./../assets/img/artist-video-poster.jpg" alt="artist-video-poster">
                <a href="#">
                    <img class="position-absolute top-50 start-50 translate-middle" src="./../assets/img/icon-youtube-play.png" alt="icon-youtube-play">
                </a>
                </div>
            </div>

            <div class="text-center py-5 ms_sectionBackgroundColor"> 
                <h4 class="ms_titleTestimonials">{{data.title}}</h4>
                <h4 class="fs-3"
                    v-for="(subTitle, index) in data.subTitles" 
                    :key="'subtitle testimonials '+index">

                <!-- inizio contenuto h4 -->
                {{subTitle}}
                <!-- fine contenuto h4 -->
                </h4>
            </div>

            <div class="row py-5 ms_sectionBackgroundColor">
                <div class="col card-group position-relative">

                    <div class="card mx-5" v-for="(testimonial, index) in data.testimonials" :key="'testimonial ' + index">
                        <div class="card-body" :class="active==index?'opacity-100':'opacity-25'">
                            <h5 class="card-title">{{testimonial.title}}</h5>
                            <p class="card-text">{{testimonial.paragraph}}</p>
                            <a href="#" class="d-flex align-items-center">
                                <img class="rounded-circle" :src="require(`./../assets/img/${testimonial.user.image}.jpg`)" :alt="`img ${testimonial.user.image}`">
                                <div class="ms-4 ms_author">
                                    <div>{{testimonial.user.name}}</div>
                                    <div class="mt-3">{{testimonial.user.work}}</div>
                                </div>
                            </a>
                        </div>
                    </div>

                    <i class="bi bi-chevron-left position-absolute start-0 top-50 fs-1" @click="prev()"></i>
                    <i class="bi bi-chevron-right position-absolute end-0 top-50 fs-1" @click="next()"></i>

                </div>

                <div class="text-center my-5 ms_pointer"> 
                    <i class="bi bi-dot fs-1"
                        v-for="(pallino, index) in numeroTestimonials" 
                        :key="'testimonial' + index"
                        :class="active=='testimonial'+pallino?'text-dark':''"></i>
                </div>

            </div>
        
        </div>
    </section>
</template>

<script>
    export default {
        name: "MySection3",
        props:{
            "data": Object,
        },
        data(){
            return{
                active: "testimonial2",
            }
        },
        computed:{
            numeroTestimonials(){
                //calcola la lunghezza dell'oggetto data.testimonials, alias quanti testimonial ci sono?
                return Object.keys(this.data.testimonials).length; 
            }
        },
        methods:{
            next(){

                //estrai indice dall'ultimo carattere della stringa, 
                //per costruzione dell'oggetto "data" l'ultimo cartattere sarà un numero indicante la posizione
                let indice = this.active.substring(this.active.length -1);

                indice++;
                const stringaIndice = "testimonial" + indice;

                if(this.active == "testimonial"+this.numeroTestimonials){
                    this.active = "testimonial1";
                }else{
                    this.active = stringaIndice;
                }

            },

            prev(){

                //estrai indice dall'ultimo carattere della stringa, 
                //per costruzione dell'oggetto "data" l'ultimo cartattere sarà un numero indicante la posizione
                let indice = this.active.substring(this.active.length -1);

                indice--;
                const stringaIndice = "testimonial" + indice;

                if(this.active == "testimonial1"){
                    this.active = "testimonial"+this.numeroTestimonials;
                }else{
                    this.active = stringaIndice;
                }

            }
        }
    }
</script>

<style lang="scss" scoped>

    @import "./../assets/variables.scss";

    section{
        position: relative;

        & .ms_shape3{
            background-image: url("./../assets/img/maxcoach-shape-03.png");
            background-size: contain;
            background-repeat: no-repeat;

            height: 15rem;
            width: 15rem;

            position: absolute;
            top: -5rem;
            left: 20rem;

        }

        & .ms_shape4{
            background-image: url("./../assets/img/maxcoach-shape-04.png");
            background-size: contain;
            background-repeat: no-repeat;

            height: 8rem;
            width: 8rem;

            position: absolute;
            top: -2rem;
            left: 25rem;

        }

        & .ms_shape5{
            background-image: url("./../assets/img/maxcoach-shape-05.png");
            background-size: contain;
            background-repeat: no-repeat;

            height: 8rem;
            width: 8rem;

            position: absolute;
            top: 29rem;
            left: 87rem;

            z-index: 9;

        }

        & .ms_ring{
            background-image: url("./../assets/img/maxcoach-shape-ring.png");
            background-size: contain;
            background-repeat: no-repeat;

            height: 8rem;
            width: 8rem;

            position: absolute;
            top: 8rem;
            left: 88rem;

            z-index: 9;

        }

        & .ms_wave{
            background-image: url("./../assets/img/wave.png");
            background-size: contain;
            background-repeat: no-repeat;

            height: 30rem;
            width: 100vw;

            position: absolute;
            bottom: 40rem;
            

        }
          
    }

    .container-fluid{
        margin: 5rem auto;

        .ms_sectionBackgroundColor{
            background-color: #faf8f6;
        }

        .card{
            
            img{
                width: 5rem;
            }

            a{
                text-decoration: none;
                
                .ms_author{
                    color: #000;

                    & div:first-child{
                        font-weight: bold;
                    }

                    & div:nth-child(2){
                        color: $dustyGray;
                    }
                }

            }
 
        }

        .ms_titleTestimonials{
            font-family: "Comforter";
            color: $colorMartin;
            font-size: 3rem;
            
        }

        .ms_pointer{
            color: $silver;
        }
       
       
    }
    
</style>