<script setup>
import BreezeApplicationLogo from '@/Components/ApplicationLogo.vue';
import { Link } from '@inertiajs/inertia-vue3';
</script>

<template>
    <div class="min-h-screen flex flex-col sm:justify-center items-center pt-6 sm:pt-0 bg-gray-100 back">
        
        <div>
            
                <BreezeApplicationLogo class="w-20 fill-current text-gray-500" style=" height: 71px;    margin-bottom: 22px;"/>
        </div>

        
            <slot />
       
    
    </div>
</template>
 <style scoped>
    .back{
        background: url('/img/background.gif');
        max-width: 1496px;
    }
    
    @media only screen and (min-width:1496px){
        .back{
            background: url('/img/background.gif');
            background-repeat: repeat;
            max-width: 100%; 
        }   
    }
 </style>