<template>
    <footer>

        <div id="ms_footerTop" class="container-fluid">
            <div class="row">
                <div class="col">

                    <div class="ms_imgFooter left">
                        <img src="./../assets/img/artist-shape-color-paint-top-left-300x170.png" alt="">
                    </div>

                    <div class="d-flex justify-content-center align-items-center h-100">
                        <span class="ms_textFooter">Newsletter to get in touch</span>
                        <div class="ms_contenitoreEmail">
                            <form>
                                <input class="ms_email" type="email" placeholder="Your e-mail">
                            </form>
                            <button class="ms_btnSendEmail" @click.prevent="inviaEmail()"><i class="bi bi-arrow-right"></i></button>
                        </div>
                    </div>

                    <div class="ms_imgFooter right">
                        <img src="./../assets/img/artist-shape-color-paint-bottom-right-300x153.png" alt="">
                    </div>

                </div>
            </div>
        </div>

       <div id="footerBottom" class="container my-5">
            <div class="row">
                <!-- <MenuFooter :menuFooter="menuFooter"/> -->
                <div class="col-4">
                    <MenuFooter :menu="menuFooter.address"/>
                </div>
                <div class="col-2">
                    <MenuFooter :menu="menuFooter.explore"/>
                </div>
                <div class="col-2">
                    <MenuFooter :menu="menuFooter.information"/>
                </div>
                <div class="col-4">
                    <MenuFooter :menu="menuFooter.instagram"/>
                </div>
            </div>
        </div>

        <div class="d-flex justify-content-center ms_copyright">&copy; 2020 Maxcoach. All Rights Reserved</div>

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

    #ms_footerTop{
        background-color: $bayOfMany;
        overflow: hidden;
        position: relative;

        .ms_imgFooter{
            position: absolute;
            bottom: 0;
            
            &.left{
                left: 0;
            }

            &.right{
                right: 0;
            }
        }

        .ms_textFooter{
            color: $white;
            font-size: 2rem;
            text-align: end;

            width: 17rem;
            margin: 2rem 8rem;
        }

        .ms_contenitoreEmail{
            position: relative;

            input.ms_email{
                width: 35rem;

                background-color: $bayOfMany;
                color: $white;

                font-size: 1.5rem;

                border-top: none;
                border-left: none;
                border-right: none;

                
            }

            .ms_btnSendEmail{
                background-color: $bayOfMany;
                border: none;

                font-size: 1.5rem;
                color: $white;

                position: absolute;
                top: 0;
                right: 0;    
            }
        }
        
    }

    .ms_copyright{
        font-size: 0.8rem;
        color: $dustyGray;
    }

</style>