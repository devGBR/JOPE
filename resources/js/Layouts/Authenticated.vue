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
  <nav
    class="p-3 border-gray-200 bg-gray-50 dark:bg-gray-800 dark:border-gray-700"
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

  <!-- Page Content -->
  <div class="main">
    <main>
      <slot />
    </main>
    <!-- SideBar -->
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
    
  </div>
</template>
<style scoped>
.main {
  max-width: 1480 !important;
  display: flex;
  justify-content: space-between;
}
.column{
    min-height: 670px;
    width: 55px;
    height:100%;
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
@keyframes opacity {
  50% {
    opacity: 0.5;
  }
  100% {
    opacity: 0;
  }
}
</style>