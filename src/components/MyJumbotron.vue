<template>
    <div class="container-fluid d-flex justify-content-center align-items-center"> 
        <div class="row">
            <div class="col d-flex justify-content-center">
                <div class="text-center w-75">
                    <h4 class="ms_textStyle">Hello, I'am Martin</h4> 
                    <h4>Artist Coaching and Mentoring Might Be for you.</h4>
                    <button class="btn mt-4 px-4 py-2">Get started today</button>
                </div>
                
            </div>
        </div>   
    </div>
</template>

<script>
    export default {
        name: "MyJumbotron",
    }
</script>

<style lang="scss" scoped>

    @import "./../assets/variables";

    .container-fluid{
        height: 45rem;
        background-image: url("./../assets/img/jumbotron.png");
        background-size: cover;

        .ms_textStyle{
            font-family: "Comforter";
            color: $colorMartin;
            font-size: 3rem;
        }

        .btn{
            background-color: $orange;
            color: $white;
            font-weight: bold;

            &:hover{
                background-color: $iceCold;
            }
        }


    }
</style>