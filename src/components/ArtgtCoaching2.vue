<template>
    <section class="container">

        <div class="row">
           <div class="col-6 text-center">
                <img class="my-4" src="./../assets/img/artist-quote-icon.png" alt="img artist-quote-icon">
           </div>
        </div>

        <div class="row">
            <div class="col text-center">
                <h4 class="ms_textStyle">{{goal.quote.sentence}}</h4>
                <h4 class="ms_textAuthor">{{goal.quote.author}}</h4>
            </div>
            <div class="col ms_textStyle">
                <p class="fs-5">{{goal.paragraph}}</p>
                <p class="my-5 fs-5">{{goal.Iam}}</p>
                <MyBtn :type="'light'" :text="'Get started today'"/>
            </div>
        </div>
        
    </section>
</template>

<script>

    import MyBtn from "./partials/MyBtn.vue";

    export default {
        name: "MySection2",
        props:{
            "goal": Object,
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

        h4.ms_textStyle{
            font-size: 2rem;
            padding: 0 10rem;
        }

        h4.ms_textAuthor{
            font-family: "Comforter";
            color: $colorMartin;
            font-size: 2rem;
            margin-top: 1rem;
        }

        .col.ms_textStyle{
            color: $boulder;

            .btn{
                color: $orange;
                font-weight: bold;
                background-color: $bisque;

                &:hover{
                    background-color: $iceCold;
                    color: $white;
                }
            }
        }
    }
    
</style>