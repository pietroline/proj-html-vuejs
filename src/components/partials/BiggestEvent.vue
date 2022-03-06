<template>
  <section class="my-2 d-flex align-items-center justify-content-center">

        <span>Start TOMORROW! Our biggerest event of the year...</span>
        <span class="mx-4 text-dark d-flex align-items-center">
            <i class="bi bi-clock me-3 fs-4"></i>
            <Countdown :deadline="deadline()"></Countdown>
        </span>
        <MyBtn :type="'dark'" :text="'Get ticket'"/>
  </section>
</template>

<script>

    //importo dayjs e aggiungo estenzione customPardeFormat
    const dayjs = require('dayjs')
    let customParseFormat = require('dayjs/plugin/customParseFormat')
    dayjs.extend(customParseFormat)

    //importo componente Countdown
    import Countdown from 'vuejs-countdown';

    import MyBtn from './MyBtn.vue';
    
    export default {
        name: "BiggestEvent",
        components:{
            Countdown,
            MyBtn,
        },
        methods:{
            deadline(){

                //che giorno è oggi?
                let data = dayjs().format();
                 
                //aggiungo 1 giorno a quella di oggi
                data = dayjs(data).add(1, "d");

                //converto la data in stringa Mese Giorno, Anno
                data = dayjs(data).format("MMMM DD, YYYY")

                return data;
            }
        }
        
    }
</script>

<style >
  
</style>