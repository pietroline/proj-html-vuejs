<template>
    <section class="container">

        <div class="row"> 
            <div class="col text-center mb-5">
                <h4 class="ms_upcomingEvents">Upcoming Events</h4>
                <h4 class="fs-3">Let's Work Together</h4>
            </div>
        </div>

        <div class="row row-cols-2 mb-5">

            <div class="col" v-for="(event, index) in data.events" :key="'event '+index">
                <div class="card mb-3 border-0">
                    <div class="row g-0">
                        <div class="col-md-4" :class="estraiIndice(index)>2?'order-1':''">
                            <img :src="require(`./../assets/img/${event.image}.jpg`)" class="img-fluid rounded-start" :alt="`img ${event.image}`">
                        </div>
                        <div class="col-md-8 d-flex align-items-center" :class="estraiIndice(index)>2?['order-0','text-end']:''">
                            <div class="card-body mx-3">
                                <div class="my-3 ms_colorEvent">Nov 22, 2020</div>
                                <div class="my-3 fw-bold">Storytelling Workshop</div>
                                <div class="my-3 ms_colorEvent">
                                    <i class="bi bi-geo-alt"></i>
                                    <span class="ms-2">Texas, US</span>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

        </div>   

    </section>
</template>

<script>
    export default {
        name: "MySection6",
        props:{
            "data": Object,
        },
        methods:{
            estraiIndice(indice){
                //questo metodo fa affidamento sul nome delle proprietà dell'oggetto
                //di fatto indice è il nome della proprietà di data.events.eventx
                //poichè per costruzione sono event1, event2...
                //l'ultimo carattere del nome della proprietà è il numero dell'indice di posizione 
                return indice.substring(indice.length-1);
            }
        }
    }
</script>

<style lang="scss" scoped>

    @import "./../assets/variables.scss";

    .container{
        margin: 5rem auto;
      
        .ms_upcomingEvents{
            font-family: "Comforter";
            color: $colorMartin;
            font-size: 3rem;
            
        }

        .ms_colorEvent{
            color: $dustyGray;
        }
       
    }
    
</style>