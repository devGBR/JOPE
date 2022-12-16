<script setup>
import BreezeButton from '@/Components/Button.vue';
import BreezeCheckbox from '@/Components/Checkbox.vue';
import BreezeGuestLayout from '@/Layouts/Guest.vue';
import BreezeInput from '@/Components/Input.vue';
import BreezeLabel from '@/Components/Label.vue';
import BreezeValidationErrors from '@/Components/ValidationErrors.vue';
import { Head, Link, useForm } from '@inertiajs/inertia-vue3';

defineProps({
    canResetPassword: Boolean,
    status: String,
});


const form = useForm({
    remember: false,
    name: '',
    email: '',
    password: '',
    password_confirmation: '',
    terms: false,
});

const submit = () => {
    form.post(route('login'), {
        onFinish: () => form.reset('password'),
    });
};

const register = () => {
    form.post(route('register'), {
        onFinish: () => form.reset('password', 'password_confirmation'),
    });
};
 
</script>

<template>
  
    <BreezeGuestLayout>
        
        <Head title="Log in" />
        <div  class="w-full flipper sm:max-w-md mt-6 px-6 py-4 bg-white shadow-md overflow-hidden sm:rounded-lg">
        <label class="inline-flex relative cursor-pointer" data-v-a2ac2cea="" style="
             display: flex;
             justify-content: center;
             align-items: center;
             position: relative;
             top: -8px;
"><input type="checkbox" class="sr-only peer" value="" @click="checked" id="switch" data-v-a2ac2cea=""><span class="ml-3 text-sm font-medium text-gray-900 dark:text-gray-300" data-v-a2ac2cea="" style="
    margin-right: 12px;
">Login</span><div class="w-11 h-6 bg-img bg-gray-200 rounded-full peer peer-focus:ring-4 peer-focus:ring-blue-300 dark:peer-focus:ring-blue-800 dark:bg-gray-700 peer-checked:after:translate-x-full peer-checked:after:border-white after:content-[''] after:absolute after:top-0.5 after:left-[2px] after:bg-white after:border-gray-300 after:border after:rounded-full after:h-5 after:w-5 after:transition-all dark:border-gray-600 peer-checked:bg--600" data-v-a2ac2cea="" style="
    position: relative;
"></div>
<span class="ml-3 text-sm font-medium text-gray-900 dark:text-gray-300" data-v-a2ac2cea="">Cadastro</span>
</label>
        <BreezeValidationErrors class="mb-4" />
        
        <div v-if="status" class="mb-4 font-medium text-sm text-green-600">
            {{ status }}
        </div>
        <div>
            <div :id="giro" class="front " v-if="loginORregister">
                <form  @submit.prevent="submit">
            <div class="textbox">
                <div class="relative">
                <div class="flex absolute inset-y-0 left-0 items-center pl-3 pointer-events-none">
                    <svg class="w-6 h-6 text-gray-500 dark:text-gray-400" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"></path></svg>
                  </div>
                  
                <BreezeInput id="email" type="email" class="mt-1 block w-full transparent" v-model="form.email" required  placeholder=" "/>
                <label for="small_outlined" class=" pt-1 bg-wt absolute text-sm text-gray-500 dark:text-gray-400 duration-300 transform -translate-y-3 scale-75 top-1 z-10 origin-[0]  px-2 peer-focus:px-2 peer-focus:text-blue-600 peer-focus:dark:text-blue-500 peer-placeholder-shown:scale-100 peer-placeholder-shown:-translate-y-1/2 peer-placeholder-shown:top-1/2 peer-focus:top-1 peer-focus:scale-75 peer-focus:-translate-y-3 left-1">Email</label>
            </div>
        </div>

            <div class="mt-4">
                <div class="relative">
                <div class="flex absolute inset-y-0 left-0 items-center pl-3 pointer-events-none">
                    <svg class="w-6 h-6 text-gray-500 dark:text-gray-400" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 15v2m-6 4h12a2 2 0 002-2v-6a2 2 0 00-2-2H6a2 2 0 00-2 2v6a2 2 0 002 2zm10-10V7a4 4 0 00-8 0v4h8z"></path></svg>
                </div>
                <BreezeInput placeholder=" " id="password" type="password" class="mt-1 block w-full transparent" v-model="form.password" required autocomplete="new-password" />
                <label for="small_outlined" class=" bg-wt absolute text-sm text-gray-500 dark:text-gray-400 duration-300 transform -translate-y-3 scale-75 top-1 z-10 origin-[0]  px-2 peer-focus:px-2 peer-focus:text-blue-600 peer-focus:dark:text-blue-500 peer-placeholder-shown:scale-100 peer-placeholder-shown:-translate-y-1/2 peer-placeholder-shown:top-1/2 peer-focus:top-1 peer-focus:scale-75 peer-focus:-translate-y-3 left-1">Senha</label>

            </div>
            </div>

            <div class="block mt-4">
                <label class="flex items-center">
                    <BreezeCheckbox name="remember" v-model:checked="form.remember" />
                    <span class="ml-2 text-sm text-gray-600">Lembre-me</span>
                </label>
            </div>

            <div class="flex items-center justify-end mt-4">
                <Link v-if="canResetPassword" :href="route('password.request')" class="underline text-sm text-gray-600 hover:text-gray-900">
                    Esqueceu sua senha?
                </Link>

                <BreezeButton class="ml-4" :class="{ 'opacity-25': form.processing }" :disabled="form.processing">
                    Entrar
                </BreezeButton>
            </div>
        </form>
            </div>
            <div class="bac" v-else>
                <form @submit.prevent="register" >
            <div class="mt-6">
                <div class="relative">
                <div class="flex absolute inset-y-0 left-0 items-center pl-3 pointer-events-none">
                    <svg class="w-6 h-6 text-gray-500 dark:text-gray-400" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z"></path></svg>
                </div>
            
                <BreezeInput placeholder=" " id="name" type="text" class="mt-1 block w-full transparent" v-model="form.name" required autofocus autocomplete="name" />
                <label for="small_outlined" class=" bg-wt absolute  text-gray-500 dark:text-gray-400 duration-300 transform -translate-y-3 scale-75 top-1 z-10 origin-[0]  px-2 peer-focus:px-2 peer-focus:text-blue-600 peer-focus:dark:text-blue-500 peer-placeholder-shown:scale-100 peer-placeholder-shown:-translate-y-1/2 peer-placeholder-shown:top-1/2 peer-focus:top-1 peer-focus:scale-75 peer-focus:-translate-y-3 left-1">Nome</label>

            </div>
        </div>

            <div class="mt-6">
                
                <div class="relative">
                <div class="flex absolute inset-y-0 left-0 items-center pl-3 pointer-events-none">
                    <svg class="w-6 h-6 text-gray-500 dark:text-gray-400" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"></path></svg>
                  </div>
                  
                <BreezeInput id="email" type="email" class="mt-1 block w-full transparent" v-model="form.email" required autocomplete="username"  placeholder=" "/>
                <label for="small_outlined" class=" pt-1 bg-wt absolute text-sm text-gray-500 dark:text-gray-400 duration-300 transform -translate-y-3 scale-75 top-1 z-10 origin-[0]  px-2 peer-focus:px-2 peer-focus:text-blue-600 peer-focus:dark:text-blue-500 peer-placeholder-shown:scale-100 peer-placeholder-shown:-translate-y-1/2 peer-placeholder-shown:top-1/2 peer-focus:top-1 peer-focus:scale-75 peer-focus:-translate-y-3 left-1">Email</label>
            </div>
            </div>
           
            <div class="mt-6">
                <div class="relative">
                <div class="flex absolute inset-y-0 left-0 items-center pl-3 pointer-events-none">
                    <svg class="w-6 h-6 text-gray-500 dark:text-gray-400" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 15v2m-6 4h12a2 2 0 002-2v-6a2 2 0 00-2-2H6a2 2 0 00-2 2v6a2 2 0 002 2zm10-10V7a4 4 0 00-8 0v4h8z"></path></svg>
                </div>
                <BreezeInput placeholder=" " id="password" type="password" class="mt-1 block w-full transparent" v-model="form.password" required autocomplete="new-password" />
                <label for="small_outlined" class=" bg-wt absolute text-sm text-gray-500 dark:text-gray-400 duration-300 transform -translate-y-3 scale-75 top-1 z-10 origin-[0]  px-2 peer-focus:px-2 peer-focus:text-blue-600 peer-focus:dark:text-blue-500 peer-placeholder-shown:scale-100 peer-placeholder-shown:-translate-y-1/2 peer-placeholder-shown:top-1/2 peer-focus:top-1 peer-focus:scale-75 peer-focus:-translate-y-3 left-1">Senha</label>

            </div>
        </div>
            <div class="mt-6">
                <div class="relative">
                <div class="flex absolute inset-y-0 left-0 items-center pl-3 pointer-events-none">
                    <svg class="w-6 h-6 text-gray-500 dark:text-gray-400" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 15v2m-6 4h12a2 2 0 002-2v-6a2 2 0 00-2-2H6a2 2 0 00-2 2v6a2 2 0 002 2zm10-10V7a4 4 0 00-8 0v4h8z"></path></svg>
                </div>
                <BreezeInput placeholder=" " id="password_confirmation" type="password" class="mt-1 transparent block w-full" v-model="form.password_confirmation" required autocomplete="new-password" />
                <label for="small_outlined" class=" bg-wt absolute text-sm text-gray-500 dark:text-gray-400 duration-300 transform -translate-y-3 scale-75 top-1 z-10 origin-[0]  px-2 peer-focus:px-2 peer-focus:text-blue-600 peer-focus:dark:text-blue-500 peer-placeholder-shown:scale-100 peer-placeholder-shown:-translate-y-1/2 peer-placeholder-shown:top-1/2 peer-focus:top-1 peer-focus:scale-75 peer-focus:-translate-y-3 left-1">Confirme a senha</label>

            </div>
        </div>
            <div class="flex items-center justify-end mt-4">
                <Link :href="route('login')" as="button" class="return  transition duration-75 hover:bg-gray-100 dark:hover:bg-gray-700 dark:text-white group">
                    <svg class="w-6 h-6 icon " fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 10h10a8 8 0 018 8v2M3 10l6 6m-6-6l6-6"></path></svg>
                </Link>

                <BreezeButton class="ml-4" :class="{ 'opacity-25': form.processing }" :disabled="form.processing">
                    Registrar
                </BreezeButton>
            </div>
        </form>
            </div>
        </div>
    </div>

            <!-- Register -->
       
    </BreezeGuestLayout>
</template>
<script>
export default {
    data(){
        return{
            loginORregister: true,
            giro: '',
            bac: ''
        }
    },
    methods: {
        checked(){
            this.loginORregister = !this.loginORregister
            if(this.loginORregister === false){
                this.giro = 'flipper'
                this.bac = "bac"
                
            }else{
                this.giro = 'reverseflip'
                this.bac = 'bac'
            }
        }
    }
}
</script>
<style scoped>
    .register{
        margin-left: 4px;
        padding-left: 9px;
        border: solid 1px firebrick;
        background: firebrick;
        border-radius: 39px;
        width: 78px;
        height: 73px;
        position: fixed;
        right: 486px;
        top: 247px;
        
    }
    .bg-white{
        background-color: rgb(13, 15, 33)!important;
    }
    .icon{
        width: 56px;
        height: 47px;
        padding-left: 8px;
    }
    .checkbox:checked ~ .flipper {
  transform: rotateY(180deg);
  transition: transform 2s;
}
.bg-wt{
        background-color: rgb(13, 15, 33) !important;
        border-radius: 8px;
        height: 22px;
    }
    .peer:focus ~ .peer-focus\:top-1 {
        top: -0.02rem !important ;
    }
    .bg-img{
        background-color: black;
    }
    #flipper{
	
	transform-style: preserve-3d;
    animation: aparecer;
    animation-duration: 2s;
    }
    #reverseflip{
        transform: rotateY(1deg);
        transition:  transform 3s;
       
    }
    
	
@keyframes aparecer {
    0% {
        position: relative;
        margin-left: 425px;
        left: 425px;
        opacity: 0;
    }
    30%{
        position: relative;
        margin-left: 368px;
        left: 368px;
        opacity: 0.2;
    }
    50%{
        position: relative;
        margin-left: 190px;
        left: 190px;
        opacity: 0.5;
    }
    75%{
        position: relative;
        margin-left: 85px;
        left: 85px;
        opacity: 0.7;
    }
    100%{
        position: relative;
        margin-left: 0px;
        left: 0px;
        opacity: 1;
    }
}
.bac{
	animation: aparecer;
    animation-duration: 2s;
    position: relative;
}





    
    
</style>
