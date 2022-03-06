<template>
    <ul>
        <!-- Per come è costruito l'oggetto proprietà mainTitle può essere soltanto una Stringa o un oggetto.
        Se menu.mainTitle.length > 0 significa che sto interrogando una stringa 
        e il valore tornato è il numero di caratteri.
        Quando menu.mainTitle.length == undefined significa che ho interrogato uno oggetto 
        e che posso accedere alle sue proprietà-->
        <li v-if="menu.mainTitle.length > 0">{{menu.mainTitle}}</li>
        <li v-if="menu.mainTitle.length == undefined">
            <span>{{menu.mainTitle.social}}</span>
            <span class="ms-1 ms_linkSocial">{{menu.mainTitle.linkSocial}}</span>
        </li>

        <!-- quando proprietà.menuTitle == null, li non da errori e non viene eseguito -->
        <li v-for="(linkMenu, index) in menu.menuTitle" :key="'linkMenuFooter' + index">
            <a href="#">{{linkMenu}}</a>
        </li>

        <!-- quando proprietà.menuIcon == null, li non da errori e non viene eseguito -->
        <li v-for="(icon, index) in menu.menuIcon" :key="'iconMenuFooter' + index" class="d-inline">
            <a href="#" class="me-4 fs-5">
                <i :class="icon"></i>
            </a>
        </li>

        <!-- quando proprietà.menuImg == null, li non da errori e non viene eseguito -->
        <li class="d-inline" v-for="(img, index) in menu.menuImg" :key="'imgMenuFooter' + index">
            <a href="#" class="me-3">
                <img class="ms_imgSocial" :src="require('./../../assets/img/'+img+'.jpeg')" alt="">
            </a>
        </li>


    </ul>
</template>

<script>
    export default {
        name: "MenuFooter",
        props:{
            "menu": Object,
        },
    }
</script>

<style lang="scss" scoped>

    @import "./../../assets/variables.scss";

   ul li{
        list-style: none;
        margin: 1rem 0;
        font-size: 0.8rem;

        a{
           text-decoration: none;
           color: $boulder;
        }

        .ms_linkSocial{
            color: $orange;
        }

        .ms_imgSocial{
            width: 7rem;
            height: 7rem;
            object-fit: cover;
        }

        &:hover a{
            color: $silver;
        }

        &:first-child{
            font-weight: bold;
        }
   }
  
</style>