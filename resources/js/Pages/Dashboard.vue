<script>
import BreezeAuthenticatedLayout from '../Layouts/Authenticated.vue';
import { Head } from '@inertiajs/inertia-vue3';
import Carrousel from '@/components/Carrousel.vue';

export default{
    components:{
        BreezeAuthenticatedLayout,
        Head,
        Carrousel
    },  
    data(){
        return{
            time: true,
            VerAnim: "PrimaryAnim",
        }
    },
    methods:{
        loop(){
           
        }
    },
    mounted(){
        setTimeout(() => {
            this.VerAnim = "SecondAnim"
        },4000)
        
        if(this.time === true){
                setTimeout(() => {
                    this.time = false
                },10000)
            }
    }
}
</script>

<template>
    <Head title="Home" />

    <BreezeAuthenticatedLayout>
        <div class="cruz">
            <div class="horizontal"></div>
            <div class="vertical"></div>
        </div>
        <carrousel/>
        <div class="conteudo">
        <div class="" style="
    font-family: Montserrat, MAfinest;
    font-size: 65px;
    margin-top: 35px;
    font-weight: 100;
    margin-left: 50px;
    
">
            Missões
        </div>
        <div class="" style="
    border-bottom: 3px solid;
    border-left: 3px solid;
    border-radius: 1px;
    height: 107px;
    width: 267px;
    margin-left: 78px;
    padding-left: 22px;
    padding-top: 14px;
        ">JOPE significa Jovens Orando Pregando Evangelizando</div>
        <video class=" h-auto rounded-lg border border-gray-200 dark:border-gray-700" controls style="
    position: relative;
    left: 347px;
    top: -135px;
">
  <source src="/docs/videos/flowbite.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
</div>
    </BreezeAuthenticatedLayout>
</template>

<style scoped>

    .horizontal{
        border: 8px solid rgb(255, 255, 255);
    background: rgb(162, 10, 10);
    width: 120px;
    height: 18px;
    position: relative;
    left: -50px;
    top: 50px;
    /* animation: hrt 2s; */
    animation: pulo-097ba13b 4s infinite;
    }
    .vertical{
        border: 8px solid rgb(255, 255, 255);
    background: rgb(141, 19, 19);
    width: 20px;
    height: 144px;
    position: relative;
    left: 0;
    /* top: 0px; */
    /* animation: vrt 2s; */
    animation: pulo1-097ba13b 4s infinite;
    }
    .cruz{
        
         position: absolute;
         left: 137px;
        top: 150px;
    }


    @keyframes vrt {
        0%{
            opacity: 0;
            top: 72px;
            left: 3px;
        }
        100%{
            opacity: 1;
        }
    }
    @keyframes hrt {
        0%{
            opacity: 0;
            left: 0px;
            top: 600;
        }
        100%{
            opacity: 1;
        }
    }

    @keyframes pulo {
        0% {
        /* top: 150px; */
        top: 50px;
        }

    50% {
        top: 0px;
        }

    100% {
        top: 50px;
        }
    }
    @keyframes pulo1 {
        0%{
            /* top: 183px; */
            top: 0px;
        }
        50%{
            top: -50px;
        }
        100%{
            top: 0px;
        }
    }
    @media only screen and (max-width: 1025px){
        .cruz{
            left: 68px;
            top: 150px;
        }
}
</style>