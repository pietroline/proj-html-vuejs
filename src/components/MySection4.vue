<template>
    <section class="container">

        <div class="text-center my-5"> 
            <h4 class="ms_artistCoaching">{{data.title}}</h4>
            <h4 class="fs-3"
                v-for="(subTitle, index) in data.subTitles" 
                :key="'subtitle artist coaching '+index">

            <!-- inizio contenuto h4 -->
            {{subTitle}}
            <!-- fine contenuto h4 -->

            </h4>
        </div>

        <div class="row">

            <div class="col-3" v-for="(course, index) in data.courses" :key="'course' + index">
                <div class="card border-0">
                    <img :src="require(`./../assets/img/${course.image}.jpg`)" class="card-img-top mt-5" :alt="`img ${course.image}`">
                    <div class="card-body">
                        <h5 class="my-2 ms_price">${{course.price}}</h5>
                        <h5 class="my-4 title">{{course.title}}</h5>
                        <a href="#" class="card-link">
                            <i class="bi bi-file-earmark-text me-2"></i>
                            <span>{{course.numberLessons}} Lessons</span>
                        </a>
                        <a href="#" class="card-link">
                            <i class="bi bi-person me-2"></i>
                            <span>{{course.maxStudents}} Students</span>
                        </a>
                    </div>
                </div>
            </div>     

        </div>

        
        <div class="row text-center mt-3">
            <div class="col">
                <MyBtn :type="'light'" :text="'View all courses'" :bootstrapIcon="'bi bi-arrow-right'"/>
            </div>
        </div>

    </section>
</template>

<script>

    import MyBtn from "./partials/MyBtn.vue";

    export default {
        name: "MySection6",
        props:{
            "data": Object,
        },
        components:{
            MyBtn,
        }
    }
</script>

<style lang="scss" scoped>

    @import "./../assets/variables.scss";

    .container{
        margin: 5rem auto;
      
        .ms_artistCoaching{
            font-family: "Comforter";
            color: $colorMartin;
            font-size: 3rem;
            
        }

        .card{
            position: relative;
            height: 35rem;

            .card-body{
                border: 3px solid transparent;

                .title{
                    font-size: 1.3rem;
                }

                &:hover{
                    cursor: pointer;
                    
                    border-color: $orange;
                    background-color: $white;

                    position: absolute;
                    bottom: 5rem;
                    width: 90%;
                }
            }
            
            .ms_price{
                color: $orange;
                font-weight: bold;
            }

            .card-link{
                color: $dustyGray;
            }

            a{
                text-decoration: none;

                &:hover{
                    color: $silver;
                }
            }
        }
       
    }
    
</style>