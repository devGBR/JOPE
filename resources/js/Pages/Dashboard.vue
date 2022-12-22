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
            <div :class="VerAnim" class="principal">
                <div class="versiculo">
                    “Porque Deus amou o mundo de tal maneira,<br/> 
                    que deu o seu Filho Unigênito, para que todo a<br/>
                    quele que nele crê não pereça, <br/>
                    mas tenha a vida eterna” <br/>
                    (João 3:16).
                </div>
            </div>
        </div>
        <carrousel/>
        <div id="Quem-Somos" class="conteudo">
        <div  class="titulo">
            O que é
            a JOPE?
        </div>
        <div class="borda" >
            
        <div class="text">
            JOPE significa Jovens Orando Pregando e Evangelizando
        </div>
    </div>
        <video class=" h-auto rounded-lg border border-gray-200 dark:border-gray-700" controls style="
           position: relative;
    left: 510px;
    top: -135px;
    height: 330px !important;
    width: 700px;
    border: 3px solid black !important;">
  <source src="/docs/videos/flowbite.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
</div>
<div  class="titulo">
            Camisa JOPE
        </div>
<div class="borda" ></div>
        <div class="card">
<div class="w-full max-w-sm rounded-lg shadow-md dark:bg-gray-800 dark:border-gray-700">
    <a href="#">
        <img class="p-8 rounded-t-lg" src="/docs/images/products/apple-watch.png" alt="product image" />
    </a>
    <div class="px-5 pb-5">
        <a href="#">
            <h5 class="text-xl font-semibold tracking-tight text-gray-900 dark:text-white">Camisa Branca JOPE(Vestes Brancas)</h5>
        </a>
        <div class="flex items-center mt-2.5 mb-5">
         
        </div>
        <div class="flex items-center justify-between">
            <span class="text-3xl font-bold text-gray-900 dark:text-white">R$100</span>
            <a href="#" class="text-white bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-sm px-5 py-2.5 text-center dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800">Add Carrinho</a>
        </div>
    </div>
</div>
</div>
    </BreezeAuthenticatedLayout>
</template>

<style scoped>
.principal{
    position: relative;
    width: 328px;
    left: 0px;
    top: 0px;     
}
    .horizontal{
        border: 8px solid rgb(255, 255, 255);
    background: rgb(162, 10, 10);
    width: 120px;
    height: 18px;
    position: relative;
    left: 97px;
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
    left: 149px;
    /* top: 0px; */
    /* animation: vrt 2s; */
    animation: pulo1-097ba13b 4s infinite;
    }
    .cruz{
        position: absolute;
        left: 6px;
        top: 150px;
        width: 331px;
        height: 300px;
    }

    .text{
        width: 79%;
        color: white;
        text-shadow: 
               -1px -1px 0px rgb(17, 17, 17), 
               -1px 1px 0px rgb(18, 17, 17),                    
                1px -1px 0px rgb(21, 21, 21),                  
                1px 0px 0px rgb(20, 20, 20);
    }
    .versiculo{
        font-family: Baskerville;
        font-size: 17.5px;
        color: white;
        text-shadow: 
               -1px -1px 0px rgb(17, 17, 17), 
               -1px 1px 0px rgb(18, 17, 17),                    
                1px -1px 0px rgb(21, 21, 21),                  
                1px 0px 0px rgb(20, 20, 20);
    }
    .PrimaryAnim{
        animation: PrimaryAnim 4s;
    }
    .SecondAnim{
        animation: SecondAnim  4s infinite;
    }
    .borda{
        border-bottom: 3px solid rgb(0, 0, 0);
    border-left: 3px solid rgb(0, 0, 0);
    height: 107px;
    width: 408px;
    margin-left: 112px;
    padding: 7px 0px 75px 36px;
    font-family: Montserrat, MAfinest;
    font-size: 15px;
    font-weight: 300;
    border-top-color: rgb(0, 0, 0);
    border-right-color: rgb(0, 0, 0);
    margin-top: 0px;
    }
    .titulo{
        font-family: Montserrat, MAfinest;
        font-size: 3.5rem;
        margin-top: 79px;
        font-weight: 500;
        margin-left: 90px;
        line-height: 1.2;
        color: black;
    }

    @keyframes SecondAnim {
        0%{
            top: 6px;
        }
        50%{
            top: -47px;
        }
        100%{
            top: 6px;
        }
    }
    @keyframes PrimaryAnim {
            0%{
                position: relative;
                opacity: 0;
            }
            30%{
                opacity: 0.2;
            }
            100%{
                position: relative;
                
                opacity: 1;
            }
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