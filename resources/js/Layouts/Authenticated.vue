<script>
import { Link } from "@inertiajs/inertia-vue3";
import Sidebar from "@/components/temp.vue";
export default {
  components: {
    Link,
    Sidebar,
  },
  data() {
    return {
      drawer: false,
      sidebar: '',
      insta: 'w'
    };
  },
  methods: {
    drw() {
      this.drawer = !this.drawer;
      if(this.drawer === true){
        this.sidebar = "side"
        this.insta = 'wid'
      }else{
        this.sidebar = 'closed'
        this.insta = 'w'
      }
    },
  },
};
</script>

<template>
  <div class="pg">
      <!-- Page Content -->
  <div class="main">
    <main style="width: 100%;
    margin-top: 38px;
    padding-top: 59px;
    ">
      <slot />
    </main>
    <!-- SideBar -->
    
  </div>
  <nav
    class="p-3 nav border-gray-200 bg-gray-50 dark:bg-gray-800 dark:border-gray-700"
  >
    <div class="flex flex-wrap items-center justify-between">
      <a href="#" class="flex items-center" style="padding-left: 23px">
        <img src="img/logo.png" alt="JOPE" class="h-6 mr-3 sm:h-10" />
      </a>
      <button
        data-collapse-toggle="navbar-hamburger"
        type="button"
        class=" inline-flex items-center p-2 ml-3 text-sm text-gray-500 rounded-lg hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-gray-200 dark:text-gray-400 dark:hover:bg-gray-700 dark:focus:ring-gray-600 menu"
        @click="drw"
        v-show="drawer === false"
        aria-controls="navbar-hamburger"
        aria-expanded="false"
      >
        <span class="sr-only">Open main menu</span>
        <svg
          class="w-6 h-6"
          aria-hidden="true"
          fill="currentColor"
          viewBox="0 0 20 20"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            fill-rule="evenodd"
            d="M3 5a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 10a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 15a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1z"
            clip-rule="evenodd"
          ></path>
        </svg>
      </button>
      <button
        @click="drw"
        v-if="drawer"
        type="button"
        data-drawer-dismiss="drawer-navigation"
        aria-controls="drawer-navigation"
        class=" inline-flex items-center p-2 ml-3 text-sm text-gray-500 rounded-lg hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-gray-200 dark:text-gray-400 dark:hover:bg-gray-700 dark:focus:ring-gray-600">
          <svg
            aria-hidden="true"
            class="w-5 h-5"
            fill="currentColor"
            viewBox="0 0 20 20"
            xmlns="http://www.w3.org/2000/svg">
              <path
                fill-rule="evenodd"
                d="M4.293 4.293a1 1 0 011.414 0L10 8.586l4.293-4.293a1 1 0 111.414 1.414L11.414 10l4.293 4.293a1 1 0 01-1.414 1.414L10 11.414l-4.293 4.293a1 1 0 01-1.414-1.414L8.586 10 4.293 5.707a1 1 0 010-1.414z"
                clip-rule="evenodd">
              </path>
          </svg>
        <span class="sr-only">Close menu</span>
      </button>
    </div>
  </nav>

  <div
      class="column dark:bg-gray-800" :class="sidebar">
      <ul class="space-y-2">
        <Link as="button" class="flex items-center p-2 text-base font-normal text-gray-900 rounded-lg transition duration-75 hover:bg-gray-100 dark:hover:bg-gray-700 dark:text-white group" style="padding-left: 6px; margin-left: 4px; padding-right: 10px;">
          <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 7a4 4 0 11-8 0 4 4 0 018 0zM12 14a7 7 0 00-7 7h14a7 7 0 00-7-7z"></path></svg>
          <span class="ml-3" v-if="drawer">Conta</span>
        </Link>
        <Link as="button" class="flex items-center p-2 text-base font-normal text-gray-900 rounded-lg transition duration-75 hover:bg-gray-100 dark:hover:bg-gray-700 dark:text-white group" style="padding-left: 6px; margin-left: 4px; padding-right: 10px;">
          <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 20h5v-2a3 3 0 00-5.356-1.857M17 20H7m10 0v-2c0-.656-.126-1.283-.356-1.857M7 20H2v-2a3 3 0 015.356-1.857M7 20v-2c0-.656.126-1.283.356-1.857m0 0a5.002 5.002 0 019.288 0M15 7a3 3 0 11-6 0 3 3 0 016 0zm6 3a2 2 0 11-4 0 2 2 0 014 0zM7 10a2 2 0 11-4 0 2 2 0 014 0z"></path></svg>
          <span class="ml-3" v-if="drawer">JOPE Integrantes</span>
        </Link>
        <Link as="button" class="flex items-center p-2 text-base font-normal text-gray-900 rounded-lg transition duration-75 hover:bg-gray-100 dark:hover:bg-gray-700 dark:text-white group" style="padding-left: 6px; margin-left: 4px; padding-right: 10px;">
          <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3.055 11H5a2 2 0 012 2v1a2 2 0 002 2 2 2 0 012 2v2.945M8 3.935V5.5A2.5 2.5 0 0010.5 8h.5a2 2 0 012 2 2 2 0 104 0 2 2 0 012-2h1.064M15 20.488V18a2 2 0 012-2h3.064M21 12a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
          <span class="ml-3" v-if="drawer">Missões</span>
        </Link>
        <Link as="button" class="flex items-center p-2 text-base font-normal text-gray-900 rounded-lg transition duration-75 hover:bg-gray-100 dark:hover:bg-gray-700 dark:text-white group" style="padding-left: 6px; margin-left: 4px; padding-right: 10px;">
          <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 11V7a4 4 0 00-8 0v4M5 9h14l1 12H4L5 9z"></path></svg>
          <span class="ml-3" v-if="drawer">Loja</span>
        </Link>
        <Link as="button" class="flex items-center p-2 text-base font-normal text-gray-900 rounded-lg transition duration-75 hover:bg-gray-100 dark:hover:bg-gray-700 dark:text-white group" style="padding-left: 6px; margin-left: 4px; padding-right: 10px;">
          <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5.636 18.364a9 9 0 010-12.728m12.728 0a9 9 0 010 12.728m-9.9-2.829a5 5 0 010-7.07m7.072 0a5 5 0 010 7.07M13 12a1 1 0 11-2 0 1 1 0 012 0z"></path></svg>
          <span class="ml-3" v-if="drawer">Live</span>
        </Link> 
      </ul>
    <ul class="pt-4 mt-4 space-y-2 border-t border-gray-200 dark:border-gray-700">
      <Link as="button" class="flex items-center p-2 text-base font-normal text-gray-900 rounded-lg transition duration-75 hover:bg-gray-100 dark:hover:bg-gray-700 dark:text-white group" style="padding-left: 6px; margin-left: 4px; padding-right: 10px;">
        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10.325 4.317c.426-1.756 2.924-1.756 3.35 0a1.724 1.724 0 002.573 1.066c1.543-.94 3.31.826 2.37 2.37a1.724 1.724 0 001.065 2.572c1.756.426 1.756 2.924 0 3.35a1.724 1.724 0 00-1.066 2.573c.94 1.543-.826 3.31-2.37 2.37a1.724 1.724 0 00-2.572 1.065c-.426 1.756-2.924 1.756-3.35 0a1.724 1.724 0 00-2.573-1.066c-1.543.94-3.31-.826-2.37-2.37a1.724 1.724 0 00-1.065-2.572c-1.756-.426-1.756-2.924 0-3.35a1.724 1.724 0 001.066-2.573c-.94-1.543.826-3.31 2.37-2.37.996.608 2.296.07 2.572-1.065z"></path><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z"></path></svg>
        <span class="ml-3" v-if="drawer">Configuração</span>
      </Link> 
      <a href="https://www.instagram.com/jopeserrinha/" as="button" :id="insta" class="flex items-center p-2 text-base font-normal text-gray-900 rounded-lg transition duration-75 hover:bg-gray-100 dark:hover:bg-gray-700 dark:text-white group" style="padding-left: 7px;padding-right: 9px;margin-left: 4px;">
        <img src="img/instagram.png" alt="" style="height: 24px;">
        <span class="ml-3" v-if="drawer">jopeserrinha</span>
      </a>  
      <Link :href="route('logout')" method="post" as="button" class="flex items-center p-2 text-base font-normal text-gray-900 rounded-lg transition duration-75 hover:bg-gray-100 dark:hover:bg-gray-700 dark:text-white group" style="margin-left: 4px; padding-left: 9px;">
        <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 16l4-4m0 0l-4-4m4 4H7m6 4v1a3 3 0 01-3 3H6a3 3 0 01-3-3V7a3 3 0 013-3h4a3 3 0 013 3v1"></path></svg>
        <span class="ml-3" v-if="drawer">Sair</span>
      </Link>             
    </ul>
  </div>

  <footer class="p-4 sm:p-6 dark:bg-gray-900" style="background-image: linear-gradient(180deg, #7e2432, #2a3480); width: 97%;">
    <div class="md:flex">
        <div class="mb-6 md:mb-0">
            <a href="https://flowbite.com/" class="flex items-center">
                <img src="img/logo.png" class="mr-3 h-8" alt="FlowBite Logo" style="margin-left: 23px;"/>
                
            </a>
            <div class="flex mt-2 space-x-6 sm:justify-center sm:mt-0">
            <a href="#" class="text-gray-500 hover:text-gray-900 dark:hover:text-white">
                <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true"><path fill-rule="evenodd" d="M22 12c0-5.523-4.477-10-10-10S2 6.477 2 12c0 4.991 3.657 9.128 8.438 9.878v-6.987h-2.54V12h2.54V9.797c0-2.506 1.492-3.89 3.777-3.89 1.094 0 2.238.195 2.238.195v2.46h-1.26c-1.243 0-1.63.771-1.63 1.562V12h2.773l-.443 2.89h-2.33v6.988C18.343 21.128 22 16.991 22 12z" clip-rule="evenodd" /></svg>
                <span class="sr-only">Facebook page</span>
            </a>
            <a href="#" class="text-gray-500 hover:text-gray-900 dark:hover:text-white">
                <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true"><path fill-rule="evenodd" d="M12.315 2c2.43 0 2.784.013 3.808.06 1.064.049 1.791.218 2.427.465a4.902 4.902 0 011.772 1.153 4.902 4.902 0 011.153 1.772c.247.636.416 1.363.465 2.427.048 1.067.06 1.407.06 4.123v.08c0 2.643-.012 2.987-.06 4.043-.049 1.064-.218 1.791-.465 2.427a4.902 4.902 0 01-1.153 1.772 4.902 4.902 0 01-1.772 1.153c-.636.247-1.363.416-2.427.465-1.067.048-1.407.06-4.123.06h-.08c-2.643 0-2.987-.012-4.043-.06-1.064-.049-1.791-.218-2.427-.465a4.902 4.902 0 01-1.772-1.153 4.902 4.902 0 01-1.153-1.772c-.247-.636-.416-1.363-.465-2.427-.047-1.024-.06-1.379-.06-3.808v-.63c0-2.43.013-2.784.06-3.808.049-1.064.218-1.791.465-2.427a4.902 4.902 0 011.153-1.772A4.902 4.902 0 015.45 2.525c.636-.247 1.363-.416 2.427-.465C8.901 2.013 9.256 2 11.685 2h.63zm-.081 1.802h-.468c-2.456 0-2.784.011-3.807.058-.975.045-1.504.207-1.857.344-.467.182-.8.398-1.15.748-.35.35-.566.683-.748 1.15-.137.353-.3.882-.344 1.857-.047 1.023-.058 1.351-.058 3.807v.468c0 2.456.011 2.784.058 3.807.045.975.207 1.504.344 1.857.182.466.399.8.748 1.15.35.35.683.566 1.15.748.353.137.882.3 1.857.344 1.054.048 1.37.058 4.041.058h.08c2.597 0 2.917-.01 3.96-.058.976-.045 1.505-.207 1.858-.344.466-.182.8-.398 1.15-.748.35-.35.566-.683.748-1.15.137-.353.3-.882.344-1.857.048-1.055.058-1.37.058-4.041v-.08c0-2.597-.01-2.917-.058-3.96-.045-.976-.207-1.505-.344-1.858a3.097 3.097 0 00-.748-1.15 3.098 3.098 0 00-1.15-.748c-.353-.137-.882-.3-1.857-.344-1.023-.047-1.351-.058-3.807-.058zM12 6.865a5.135 5.135 0 110 10.27 5.135 5.135 0 010-10.27zm0 1.802a3.333 3.333 0 100 6.666 3.333 3.333 0 000-6.666zm5.338-3.205a1.2 1.2 0 110 2.4 1.2 1.2 0 010-2.4z" clip-rule="evenodd" /></svg>
                <span class="sr-only">Instagram page</span>
            </a>
            <a href="#" class="text-gray-500 hover:text-gray-900 dark:hover:text-white">
                <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true"><path d="M8.29 20.251c7.547 0 11.675-6.253 11.675-11.675 0-.178 0-.355-.012-.53A8.348 8.348 0 0022 5.92a8.19 8.19 0 01-2.357.646 4.118 4.118 0 001.804-2.27 8.224 8.224 0 01-2.605.996 4.107 4.107 0 00-6.993 3.743 11.65 11.65 0 01-8.457-4.287 4.106 4.106 0 001.27 5.477A4.072 4.072 0 012.8 9.713v.052a4.105 4.105 0 003.292 4.022 4.095 4.095 0 01-1.853.07 4.108 4.108 0 003.834 2.85A8.233 8.233 0 012 18.407a11.616 11.616 0 006.29 1.84" /></svg>
                <span class="sr-only">Twitter page</span>
            </a>
        </div>
        </div>
        <div class="position">
            <div>
                <h2 class="mb-2 text-sm font-semibold text-gray-900 uppercase dark:text-white"></h2>
                <ul class="text-gray-600 dark:text-gray-400">
                    <li class="mb-3">
                        <a href="https://flowbite.com/" class="hover:underline flex">
                          <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3.055 11H5a2 2 0 012 2v1a2 2 0 002 2 2 2 0 012 2v2.945M8 3.935V5.5A2.5 2.5 0 0010.5 8h.5a2 2 0 012 2 2 2 0 104 0 2 2 0 012-2h1.064M15 20.488V18a2 2 0 012-2h3.064M21 12a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>
                          <span class="ml-2" >Mission the word</span>
                        </a>
                    </li>
                    <li class="mb-3">
                        <a href="https://tailwindcss.com/" class="hover:underline flex">
                          <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 11V7a4 4 0 00-8 0v4M5 9h14l1 12H4L5 9z"></path></svg>
                          <span class="ml-2" >Loja da JOPE Oficial</span>
                        </a>
                    </li>
                    <li class="mb-3">
                        <a href="https://tailwindcss.com/" class="hover:underline flex">
                          <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5.636 18.364a9 9 0 010-12.728m12.728 0a9 9 0 010 12.728m-9.9-2.829a5 5 0 010-7.07m7.072 0a5 5 0 010 7.07M13 12a1 1 0 11-2 0 1 1 0 012 0z"></path></svg>
                          <span class="ml-2">Live</span></a>
                    </li>
                </ul>
            </div>
        <p class="" style="    height: 172px;
    border-right: 2px solid;
    margin-left: 100px;
    margin-right: 17px;"/>
        <div class="grid grid-cols-2 gap-8 sm:gap-6 sm:grid-cols-3">
            <div>
                <h2 class="mb-2 text-sm font-semibold text-gray-900 uppercase dark:text-white">Pagina</h2>
                <ul class="text-gray-600 dark:text-gray-400">
                    <li class="mb-3">
                        <a href="#Quem-Somos" class="">quem somos</a>
                    </li>
                    <li class="mb-3">
                        <a href="https://tailwindcss.com/" class="">eventos</a>
                    </li>
                    <li class="mb-3">
                        <a href="https://tailwindcss.com/" class="">mídias</a>
                    </li>
                    <li>
                        <a href="https://tailwindcss.com/" class="">FAQ</a>
                    </li>
                </ul>
            </div>
            <div>
                <h2 class="mb-2 text-sm font-semibold text-gray-900 uppercase dark:text-white">Siga-nos</h2>
                <ul class="text-gray-600 dark:text-gray-400">
                    <li class="mb-4">
                        <a href="https://github.com/themesberg/flowbite" class="hover:underline ">Instagram</a>
                    </li>
                    <li>
                        <a href="https://discord.gg/4eeurUVvTy" class="hover:underline">Facebook</a>
                    </li>
                </ul>
            </div>
            <div>
                <h2 class="mb-2 text-sm font-semibold text-gray-900 uppercase dark:text-white">JOPERS</h2>
                <ul class="text-gray-600 dark:text-gray-400">
                    <li class="mb-3">
                        <a href="https://www.instagram.com/joperecife/" class="hover:underline">JopeRecife</a>
                    </li>
                    <li class="mb-3">
                        <a href="https://www.instagram.com/jopeoiapoque/" class="hover:underline">JopeOiapoque</a>
                    </li>
                    <li class="mb-3">
                        <a href="https://www.instagram.com/jopearaguari/" class="hover:underline">JopeAraguari</a>
                    </li>
                    <li class="">
                        <a href="https://www.instagram.com/jopemaceio_/" class="hover:underline">JopeMaceio</a>
                    </li>
                </ul>
            </div>
        </div>
    </div>
    </div>
    <hr class="my-6 border-gray-200 sm:mx-auto dark:border-gray-700 lg:my-8" style="margin-top: 0px;"/>
    <div class="sm:flex sm:items-center sm:justify-between">
        <span class="text-sm text-gray-500 sm:text-center dark:text-gray-400">© 2022 <a href="https://JOPEMoviment.com" class="hover:underline">JOPEMoviment™</a>. Tudo por Cristo✝️.
        </span>
        
    </div>
</footer>
</div>
</template>
<style scoped>
.position {
  display: flex;
    position: relative;
    left: 171px;
}
.main {
  max-width: 1480 !important;
  display: flex;
  justify-content: space-between;
  
  min-height: 733px;
}
.pg{
  background-image: linear-gradient(352deg, #912121, #2a3480);
}
a:hover{
  text-decoration: none !important;
}
.h-8{
  height: 4rem;
    width: 298px;
}
.column{
    min-height: 670px;
    width: 55px;
    position: fixed;
    top: 63px;
    right: 0px;
    display: grid;
    align-content: space-between;
}
#wid{
  width: 142px;
}
#w{
  width: 40px;
}
.side{
    width: 200px;
    transition: width 1s;
}
.closed{
  width: 55px;
  transition: width 1s;
}
.menu:hover {
  color: #b32c2c;
  transition: 1.5s;
}
.menu:active {
  transition: 2s;
  animation: opacity;
}
.nav{
  position: fixed;
  width: 100%;
  max-width: 1490px;
  flex-direction: column;
  top: 0;
}

@keyframes opacity {
  50% {
    opacity: 0.5;
  }
  100% {
    opacity: 0;
  }
}
@media only screen and (min-width: 320px){
        .column{
            min-height: 615px;
        }
}
@media only screen and (min-width: 375px){
        .column{
            min-height: 615px;
        }
}
@media only screen and (max-width: 414px){
        .column{
            min-height: 833px;
        }
        .main{
          min-height: 897px;
        }
}
@media only screen and (min-width: 425px){
        .column{
            min-height: 615px;
        }
}
@media only screen and (min-width: 768px){
        .column{
            min-height: 670px;
        }
}
@media only screen and (max-width: 1025px){
        .column{
            min-height: 615px;
        }
}
</style>