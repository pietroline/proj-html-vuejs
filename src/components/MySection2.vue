<template>
    <section class="container">

        <div class="row">
           <div class="col-6 text-center">
                <img class="my-4" src="./../assets/img/artist-quote-icon.png" alt="img artist-quote-icon">
           </div>
        </div>

        <div class="row">
            <div class="col text-center">
                <h4 class="textStyle">I coach and mentor visual artists, like you, to Create Like You Mean It</h4>
                <h4 class="textAuthor">Martin Garrix</h4>
            </div>
            <div class="col textStyle">
                <p class="fs-5">As a coach and mentor, my ultimate goal is to motivate visual artists toward inspired action. I help you get you back on track to being the productive, creative, meaaningful and authentic artist you truly want to be. I support artists in crafting and living a creative life as well as feeling good about themselves and their art.</p>
                <p class="my-5 fs-5">As an artist and an educator for nearly 30 years, I understand  what it takes to create.</p>
                <button class="btn px-4 py-2">Get started today</button>
            </div>
        </div>
        
             
       
        
    </section>
</template>

<script>
    export default {
        name: "MySection2",
    }
</script>

<style lang="scss" scoped>

    @import "./../assets/variables.scss";

    .container{
        margin: 5rem auto;

        h4.textStyle{
            font-size: 2rem;
            padding: 0 10rem;
        }

        h4.textAuthor{
            font-family: "Comforter";
            color: $colorMartin;
            font-size: 2rem;
            margin-top: 1rem;
        }

        .col.textStyle{
            color: $boulder;

            .btn{
                color: $orange;
                font-weight: bold;
                background-color: $bisque;

                &:hover{
                    background-color: $iceCold;
                    color: #fff;
                }
            }
        }
    }
    
</style>