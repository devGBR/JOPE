<script setup>
import BreezeApplicationLogo from '@/Components/ApplicationLogo.vue';
import { Link } from '@inertiajs/inertia-vue3';
</script>

<template>
    <div class="min-h-screen flex flex-col sm:justify-center items-center pt-6 sm:pt-0 bg-gray-100">
        <img src="img/background.gif" class="back" alt="">
        <div class="principal">
        <div>
            
                <BreezeApplicationLogo class="w-20 fill-current text-gray-500" style=" height: 71px;    margin: 0 auto;"/>
        </div>

        
            <slot />
       
        </div>
    </div>
</template>
 <style scoped>
    .back{
       width: 100%;
       position: fixed; 
        
    }
    .principal{
        position: relative;
    }
    
    @media only screen and (min-width:1496px){
        .back{
            background: url('/img/background.gif');
            background-repeat: repeat;
            max-width: 100%; 
        }   
    }
 </style>