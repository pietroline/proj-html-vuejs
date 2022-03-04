<template>
    <section class="container-fluid">

        <div class="row row-cols-1">
            <div class="col text-center position-relative">
               <img src="./../assets/img/artist-video-poster.jpg" alt="artist-video-poster">
               <a href="#">
                   <img class="position-absolute top-50 start-50 translate-middle" src="./../assets/img/icon-youtube-play.png" alt="icon-youtube-play">
               </a>
            </div>
        </div>

        <div class="text-center my-5"> 
            <h4 class="ms_titleTestimonials">Testimonials</h4>
            <h4 class="fs-3">Why do people love me?</h4>
        </div>

        <div class="row my-5">

            <div class="col card-group">
                <div class="card mx-5 opacity-25">
                    <div class="card-body">
                        <h5 class="card-title">It's a choice of quality fot people with special needs</h5>
                        <p class="card-text">I'm a very strict person so I require everithing to be organized and neat. Then, I'll be abble to make thimks right and shine. MaxCoach guys got me.</p>
                        <a href="#" class="d-flex align-items-center">
                            <img class="rounded-circle" src="./../assets/img/artist-testimonial-avatar-01.jpg" alt="img artist-testimonial-avatar-01">
                            <div class="ms-4 ms_author">
                                <div>Florence Themes</div>
                                <div class="mt-3">/Multimedia Admin</div>
                            </div>
                        </a>
                    </div>
                </div>

                <div class="card mx-5">
                    <div class="card-body">
                        <h5 class="card-title">High level of efficiency and scientific teaching methods</h5>
                        <p class="card-text">I am free to lear at my own pace, follow my own schedule and choose the subject I want to learn from the syllabus. Great study portal for people like me</p>
                        <a href="#" class="d-flex align-items-center">
                            <img class="rounded-circle" src="./../assets/img/artist-testimonial-avatar-02.jpg" alt="img artist-testimonial-avatar-02">
                            <div class="ms-4 ms_author">
                                <div>Mina Hollance</div>
                                <div class="mt-3">/ Freelancer</div>
                            </div>
                        </a>
                    </div>
                </div>

                <div class="card mx-5 opacity-25">
                    <div class="card-body">
                        <h5 class="card-title">Professional team of specialists and passionate mentors at teach</h5>
                        <p class="card-text">I need to get a certification for English profiency and MaxCoach is my best choice. Their tutors are smart and professional when dealing with students.</p>
                        <a href="#" class="d-flex align-items-center">
                            <img class="rounded-circle" src="./../assets/img/artist-testimonial-avatar-03.jpg" alt="img artist-testimonial-avatar-03">
                            <div class="ms-4 ms_author">
                                <div>Madley Pondor</div>
                                <div class="mt-3">/IT Specialist</div>
                            </div>
                        </a>
                    </div>
                </div>
            </div>

            <div class="text-center my-5 ms_pointer"> 
               <i class="bi bi-dot fs-1"></i>
               <i class="bi bi-dot fs-1"></i>
               <i class="bi bi-dot fs-1"></i>
               <i class="bi bi-dot fs-1"></i>
            </div>

        </div>
        
             
       
        
    </section>
</template>

<script>
    export default {
        name: "MySection3",
    }
</script>

<style lang="scss" scoped>

    @import "./../assets/variables.scss";

    .container-fluid{
        margin: 5rem auto;

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
            & i:first-child{
                color: #000;
            }
        }
       
       
    }
    
</style>