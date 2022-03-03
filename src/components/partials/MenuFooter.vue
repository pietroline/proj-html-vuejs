<template>
<div class="col d-flex justify-content-between">

    <div  v-for="(proprieta, index) in (Object.keys(menuFooter).length, menuFooter) " :key="'menuFooter ' + index">
                        
        <ul>

            <!-- Per come è costruito l'oggetto proprietà mainTitle può essere soltanto una Stringa o un oggetto.
                Se proprieta.mainTitle.length > 0 significa che sto interrogando una stringa 
                e il valore tornato è il numero di caratteri.
                Quando proprieta.mainTitle.length == undefined significa che ho interrogato uno oggetto 
                e che posso accedere alle sue proprietà-->
            <li v-if="proprieta.mainTitle.length > 0">{{proprieta.mainTitle}}</li>
            <li v-if="proprieta.mainTitle.length == undefined">
                <span>{{proprieta.mainTitle.social}}</span>
                <span class="ms-1 linkSocial">{{proprieta.mainTitle.linkSocial}}</span>
            </li>

            <!-- quando proprietà.menuTitle == null, li non da errori e non viene eseguito -->
            <li v-for="(linkMenu, index) in proprieta.menuTitle" :key="'linkMunuFooter' + index">
                <a href="#">{{linkMenu}}</a>
            </li>

                <!-- quando proprietà.menuImg == null, li non da errori e non viene eseguito -->
            <li class="d-flex">
                <div v-for="(img, index) in proprieta.menuImg" :key="'imgMunuFooter' + index" class="mx-2">
                    <a href="#">
                        <div class="imgSocial">
                            <img class="w-100 h-100" :src="`./../assets/img/${img}`" alt="">
                        </div>
                    </a>
                </div>
            </li>

        </ul>                                            
    </div>

</div>
</template>

<script>
    export default {
        name: "MenuFooter",
        props:{
            "menuFooter": Object,
        }
    }
</script>

<style lang="scss" scoped>

    @import "./../../assets/variables.scss";

    ul li{
        font-size: 0.8rem;
        margin: 1rem 0;
        list-style: none;

        a{
            color: $boulder;
            text-decoration: none;
        }

        .linkSocial{
            color: $tulipTree;
        }

        .imgSocial{
            width: 7rem;
            height: 7rem;
        }
    }

    ul li:first-child{
        font-weight: bold;
    }
</style>