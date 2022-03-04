<template>
    <section class="container">

        <div class="text-center my-5"> 
            <h4 class="upcomingEvents">Upcoming Events</h4>
            <h4 class="fs-3">Let's Work Together</h4>
        </div>

        <div class="row mb-5">

            <div class="col card mb-3 mx-3 border-0">
                <div class="row g-0">
                    <div class="col-md-4">
                        <img src="./../assets/img/artist-event-04-250x300.jpg" class="img-fluid rounded-start" alt="img artist-event-04">
                    </div>
                    <div class="col-md-8 d-flex align-items-center">
                        <div class="card-body">
                            <div class="my-3 colorEvent">Nov 22, 2020</div>
                            <div class="my-3 fw-bold">Storytelling Workshop</div>
                            <div class="my-3 colorEvent">
                                <i class="bi bi-geo-alt"></i>
                                <span class="ms-2">Texas, US</span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <div class="col card mb-3 mx-3 border-0">
                <div class="row g-0">
                    <div class="col-md-4">
                        <img src="./../assets/img/artist-event-03-250x300.jpg" class="img-fluid rounded-start" alt="img artist-event-03">
                    </div>
                    <div class="col-md-8 d-flex align-items-center">
                        <div class="card-body">
                            <div class="my-3 colorEvent">OCT 10, 2020</div>
                            <div class="my-3 fw-bold">Painting Art Contest 2020</div>
                            <div class="my-3 colorEvent">
                                <i class="bi bi-geo-alt"></i>
                                <span class="ms-2">New York, US</span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

        </div>

        <div class="row">

            <div class="col card mb-3 mx-3 border-0">
                <div class="row g-0">
                    <div class="col-md-8 d-flex align-items-center">
                        <div class="card-body text-end mx-3">
                            <div class="my-3 colorEvent">Nov 23, 2020</div>
                            <div class="my-3 fw-bold">International Art Fair 2020</div>
                            <div class="my-3 colorEvent">
                                <i class="bi bi-geo-alt"></i>
                                <span class="ms-2">Hamburg, Germany</span>
                            </div>
                        </div>
                    </div>
                    <div class="col-md-4">
                        <img src="./../assets/img/artist-event-02-250x300.jpg" class="img-fluid rounded-start" alt="img artist-event-02">
                    </div>
                </div>
            </div>

            <div class="col card mb-3 mx-3 border-0">
                <div class="row g-0">
                    <div class="col-md-8 d-flex align-items-center">
                        <div class="card-body text-end mx-3">
                            <div class="my-3 colorEvent">Dec 15, 2020</div>
                            <div class="my-3 fw-bold">Street Performace: Call for Artist</div>
                            <div class="my-3 colorEvent">
                                <i class="bi bi-geo-alt"></i>
                                <span class="ms-2">Illinois, US</span>
                            </div>
                        </div>
                    </div>
                    <div class="col-md-4">
                        <img src="./../assets/img/artist-event-01-250x300.jpg" class="img-fluid rounded-start" alt="img artist-event-01">
                    </div>
                </div>
            </div>

        </div>

        

    
        <!-- artist-event-01-250x300.jpg -->
    </section>
</template>

<script>
    export default {
        name: "MySection6",
    }
</script>

<style lang="scss" scoped>

    @import "./../assets/variables.scss";

    .container{
        margin: 5rem auto;
      
        .upcomingEvents{
            font-family: "Comforter";
            color: $colorMartin;
            font-size: 3rem;
            
        }

        .colorEvent{
            color: $dustyGray;
        }
       
    }
    
</style>