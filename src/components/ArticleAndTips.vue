<template>
    <section class="py-2">
        <div class="container">

            <div class="row text-center my-5"> 
                <div class="col">
                    <h4 class="ms_articleAndTips">{{title}}</h4>
                    <h4 class="fs-2" 
                        v-for="(subTitle, index) in subTitles" 
                        :key="'subtitle '+index">

                    <!-- inizio contenuto h4 -->
                    {{subTitle}}
                    <!-- fine contenuto h4 -->

                    </h4>
                </div>
            </div>

            <div class="row">

                <div class="col-3">
                    <div class="card left border-0">
                        <div class="contenitoreImg">
                            <div class="overlay dark"/>
                            <img :src="require(`./../assets/img/${data.event1.image}.jpeg`)" class="card-img-top" :alt="`img ${data.event1.image}`">
                        </div>
                        <div class="card-body">
                            <div class="ms_work mt-3">{{data.event1.type}}</div>
                            <h5 class="card-title mb-4">{{data.event1.title}}</h5>
                            <div class="ms_info">
                                <i class="bi bi-calendar me-1"></i>
                                <span>{{data.event1.date}}</span>
                            </div>
                            <div class="ms_info">
                                <i class="bi bi-eye me-1"></i>
                                <span>{{data.event1.views}} views</span>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="col-6 p-5">
                    <div class="card border-0 text-white">

                        <div class="contenitoreImg">
                            <div class="overlay light"/>
                             <img :src="require(`./../assets/img/${data.mainEvent.image}.jpeg`)" class="card-img-top" :alt="`img ${data.mainEvent.image}`">
                        
                            <div class="card-body position-absolute bottom-0">
                                <div class="ms_work text-white">{{data.mainEvent.type}}</div>
                                <h5 class="card-title mb-4">{{data.mainEvent.title}}</h5>
                                <div class="ms_info text-white">
                                    <i class="bi bi-calendar me-1"></i>
                                    <span>{{data.mainEvent.date}}</span>
                                </div>
                                <div class="ms_info text-white">
                                    <i class="bi bi-eye me-1"></i>
                                    <span>{{data.mainEvent.views}} views</span>
                                </div>
                            </div>
                        </div>

                    </div>
                </div>

                <div class="col-3">
                    <div class="card right border-0">
                        <div class="contenitoreImg">
                            <div class="overlay dark"/>
                             <img :src="require(`./../assets/img/${data.event2.image}.jpeg`)" class="card-img-top" :alt="`img ${data.event2.image}`">
                        </div>
                        <div class="card-body">
                            <div class="ms_work mt-3">{{data.event2.type}}</div>
                            <h5 class="card-title mb-4">{{data.event2.title}}</h5>
                            <div class="ms_info">
                                <i class="bi bi-calendar me-1"></i>
                                <span>{{data.event2.date}}</span>
                            </div>
                            <div class="ms_info">
                                <i class="bi bi-eye me-1"></i>
                                <span>{{data.event2.views}} views</span>
                            </div>
                        </div>
                    </div>
                </div>

            </div>

            <div class="row">
                <div class="col">
                    <div class="text-center mt-5">
                        <span class="ms_info">Get into details now?</span>
                        <a href="#" class="ms_info color">View all posts <i class="bi bi-arrow-right"></i></a>
                    </div>
                </div>
            </div>

        </div>
    </section>
</template>

<script>
    export default {
        name: "MySection5",
        props:{
            "title": String,
            "subTitles": Array,
            "data": Object,
        }
    }
</script>

<style lang="scss" scoped>

    @import "./../assets/variables.scss";

    section{
        background-color: $backgroundSection5;
    }

    .container{
        margin: 5rem auto;
        
        .ms_articleAndTips{
            font-family: "Comforter";
            color: $colorMartin;
            font-size: 3rem;
            
        }

        .ms_info{
            color: $dustyGray;
            display: inline;
            margin-right: 1rem;
            text-decoration: none;

            &:hover{
                color: $silver;
            }
        }

        .ms_info.color{
            color:$orange;

            &:hover{
                color: $crimson;
            }
        }
      
        .card{
            cursor: pointer;
            box-shadow: 0rem 2rem 5rem -3rem #000;

            &.left{
                margin-top: 20rem;
            }

            &.right{
                margin-top: 5rem;
            }

            .contenitoreImg{
                position: relative;

                .overlay{

                    position: absolute;
                    top: 0px;
                    left: 0px;
                    width: 100%;
                    height: 100%;

                    &.light{
                        background-color: rgba(0, 0, 0, 0.2);
                    }
                    &.dark{
                        background-color: rgba(0, 0, 0, 0.1);
                    }
                }
                    
            }

            &:hover .overlay{
                &.light{
                    background-color: rgba(0, 0, 0, 0.1);    
                }

                &.dark{
                    background-color: rgba(0, 0, 0, 0.2);
                }
                
            }
            

            .ms_work{
                color: $dustyGray;
                font-weight: bold;
                margin-bottom: 0.5rem;
            }
        
        }
       
    }
    
</style>