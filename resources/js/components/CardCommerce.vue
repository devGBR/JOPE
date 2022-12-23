<template>
    <div
        class="w-full max-w-sm rounded-lg shadow-md dark:bg-gray-800 dark:border-gray-700"
        data-v-097ba13b=""
        >
        <a href="#" data-v-097ba13b="">
          <img
            class="p-8 rounded-t-lg"
            :src="img"
            alt="product image"
            data-v-097ba13b=""/>
        </a>
        <div class="px-5 pb-5" data-v-097ba13b="">
          <a href="#" data-v-097ba13b="">
            <h5
              class=" text-xl font-semibold tracking-tight text-gray-900 dark:text-white"
              data-v-097ba13b="">
              {{ Titleitem }}
            </h5>
        </a>
          <div class="flex items-center mt-2.5 mb-5" data-v-097ba13b=""></div>
          <div class="flex items-center justify-between" data-v-097ba13b="">
            <span
              class="text-3xl font-bold text-gray-900 dark:text-white"
                  data-v-097ba13b="">
                    R${{Price}}    
            </span>
            <a
              href="#"
              class=" text-white bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-sm px-5 py-2.5 text-center dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800"
              data-v-097ba13b="">
              Add Carrinho
            </a>
          </div>
        </div>
      </div>
</template>
<script>
export default {
    props: {
        Price: {
            type: Number,
            required: false,
            default: '0'
        },
        Titleitem: {
            type: String,
            required: false,
            default: ''
        },
        img: {
            type: String,
            required: false,
            default: ''
        },

    }, 
}
</script>