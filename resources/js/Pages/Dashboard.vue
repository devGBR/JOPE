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
        
    </BreezeAuthenticatedLayout>
</template>

<style scoped>
    .horizontal{
        border: 8px solid black;
    background: rgb(60, 60, 60);
    width: 120px;
    height: 18px;
    position: relative;
    left: -50px;
    top: 50px;
    /* animation: hrt 2s; */
    animation: pulo-097ba13b 4s infinite;
    }
    .vertical{
        border: 8px solid black;
    background: rgb(60, 60, 60);
    width: 20px;
    height: 144px;
    position: relative;
    left: 0;
    /* top: 0px; */
    /* animation: vrt 2s; */
    animation: pulo1-097ba13b 4s infinite;
    }
    .cruz{
        
         position: fixed;
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
        top: 5px;
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