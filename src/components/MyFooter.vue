<template>
    <footer>

        <div id="footerTop" class="container-fluid">
            <div class="row">
                <div class="col">

                    <div class="imgFooter left">
                        <img src="./../assets/img/artist-shape-color-paint-top-left-300x170.png" alt="">
                    </div>

                    <div class="d-flex justify-content-center align-items-center h-100">
                        <span class="textFooter">Newsletter to get in touch</span>
                        <div class="contenitoreEmail">
                            <form>
                                <input class="email" type="email" placeholder="Your e-mail">
                            </form>
                            <button class="btnSendEmail" @click.prevent="inviaEmail()"><i class="bi bi-arrow-right"></i></button>
                        </div>
                    </div>

                    <div class="imgFooter right">
                        <img src="./../assets/img/artist-shape-color-paint-bottom-right-300x153.png" alt="">
                    </div>

                </div>
            </div>
        </div>

       <div id="footerBottom" class="container my-5">
            <div class="row">
                <MenuFooter :menuFooter="menuFooter"/>
            </div>
        </div>

        <div class="container d-flex justify-content-center copyright">&copy; 2020 Maxcoach. All Rights Reserved</div>

    </footer>
</template>

<script>

    import MenuFooter from "./partials/MenuFooter.vue";

    export default {
        name: "MyFooter",
        components:{
            MenuFooter,
        },
        props:{
            "menuFooter": Object,
        },
        methods:{
            inviaEmail(){
                //il comportamento assundo dalla input quando premuto il tasto enter è quello di ricaricare la pagina
                //simulo il comportamento anche quando viene inviata la email premendo il button
                window.location.reload(true);
            },
        },

    }
</script>

<style lang="scss" scoped>

    @import "./../assets/variables.scss";

    #footerTop{
        background-color: $bayOfMany;
        overflow: hidden;
        position: relative;

        .imgFooter{
            position: absolute;
            bottom: 0;
            
            &.left{
                left: 0;
            }

            &.right{
                right: 0;
            }
        }

        .textFooter{
            color: #fff;
            font-size: 2rem;
            text-align: end;

            width: 17rem;
            margin: 2rem 8rem;
        }

        .contenitoreEmail{
            position: relative;

            input.email{
                width: 35rem;

                background-color: $bayOfMany;
                color: #fff;

                font-size: 1.5rem;

                border-top: none;
                border-left: none;
                border-right: none;

                
            }

            .btnSendEmail{
                background-color: $bayOfMany;
                border: none;

                font-size: 1.5rem;
                color: #fff;

                position: absolute;
                top: 0;
                right: 0;    
            }
        }
        
    }

    .copyright{
        font-size: 0.8rem;
        color: $dustyGray;
    }

</style>