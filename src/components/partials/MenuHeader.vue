<template>
    <nav>
        
        <ul class="nav">
            <li v-for="(menu, indice) in menuHeader" 
                :key="'voce menu header' + indice">

                <!-- inizio contenuto li -->
                <a class="nav-link text-dark" href="#">
                    <span>{{menu}}</span>
                    <i class="bi bi-chevron-down"></i>
                </a>
                <!-- fine contenuto li -->
            </li>
        </ul>
        
    </nav>
</template>

<script>
    export default {
        name: "MenuHeader",
        props:{
            "menuHeader": Array,
        }
    }
</script>

<style scoped>

    .bi-chevron-down{
        font-size: 0.6rem;
        margin-left: 0.3rem;
    }

</style>