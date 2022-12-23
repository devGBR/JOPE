<script>
import BreezeAuthenticatedLayout from "../Layouts/Authenticated.vue";
import { Head } from "@inertiajs/inertia-vue3";
import Carrousel from "@/components/Carrousel.vue";
import Video from "@/components/video.vue";
import CardCommerce from "@/components/CardCommerce.vue";
import CruzAnimation from '@/components/CruzAnimation.vue';

export default {
  components: {
    BreezeAuthenticatedLayout,
    Head,
    Carrousel,
    Video,
    CardCommerce,
    CruzAnimation
},
};
</script>

<template>
  <Head title="Home" />

  <BreezeAuthenticatedLayout>
    <cruz-animation/>
    <carrousel />
    <div id="Quem-Somos" class="conteudo">
      <div class="titulo">O que é a JOPE?</div>
      <div class="borda">
        <div class="text">
          JOPE significa Jovens Orando Pregando e Evangelizando
        </div>
      </div>
        <Video/>
    </div>
    <div class="camisa">
    
    <div class="secondborda" style="
    padding-left: 22px;
    padding-bottom: 0px;
    padding-top: 1px;
    ">
        <div 
            class="secondtitulo" 
            style="
            margin-top: 0px;
            margin-left: 0px;">
                Camisa JOPE
        </div>
    </div>
    </div>
    <div
      class="card"
      data-v-097ba13b=""
      style="
        padding-top: 9px;
        padding-bottom: 39px;
        padding-left: 10px;
        padding-right: 0px;">
        <CardCommerce 
            Titleitem="Camisa Branca JOPE(Luz do Mundo)"
            Price="100"  
            style="position: relative; left: 9px; top: 7px;"
        />
        <CardCommerce 
            Titleitem="Camisa Preta JOPE(...)"
            Price="100" 
            style="
            position: relative;     
            left: 60px !important;
            top: 7px;"
        />
    </div>
        <div class="Posts">
            <div class="titulo">O que está acontecendo?</div>
                <div class="borda" style="width:87%;">
                     <div class="text" style="padding-right: 58%;">
                        Veja o que está acontecendo nas Redes Sociais da JOPE!
                    </div>
                </div>
                <div class="postsdarede">
                    <div class="border">
                        <div class="postagens">
                            
                    </div>
                    <svg class="w-5 h-5 text-white" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true"><path fill-rule="evenodd" d="M12.315 2c2.43 0 2.784.013 3.808.06 1.064.049 1.791.218 2.427.465a4.902 4.902 0 011.772 1.153 4.902 4.902 0 011.153 1.772c.247.636.416 1.363.465 2.427.048 1.067.06 1.407.06 4.123v.08c0 2.643-.012 2.987-.06 4.043-.049 1.064-.218 1.791-.465 2.427a4.902 4.902 0 01-1.153 1.772 4.902 4.902 0 01-1.772 1.153c-.636.247-1.363.416-2.427.465-1.067.048-1.407.06-4.123.06h-.08c-2.643 0-2.987-.012-4.043-.06-1.064-.049-1.791-.218-2.427-.465a4.902 4.902 0 01-1.772-1.153 4.902 4.902 0 01-1.153-1.772c-.247-.636-.416-1.363-.465-2.427-.047-1.024-.06-1.379-.06-3.808v-.63c0-2.43.013-2.784.06-3.808.049-1.064.218-1.791.465-2.427a4.902 4.902 0 011.153-1.772A4.902 4.902 0 015.45 2.525c.636-.247 1.363-.416 2.427-.465C8.901 2.013 9.256 2 11.685 2h.63zm-.081 1.802h-.468c-2.456 0-2.784.011-3.807.058-.975.045-1.504.207-1.857.344-.467.182-.8.398-1.15.748-.35.35-.566.683-.748 1.15-.137.353-.3.882-.344 1.857-.047 1.023-.058 1.351-.058 3.807v.468c0 2.456.011 2.784.058 3.807.045.975.207 1.504.344 1.857.182.466.399.8.748 1.15.35.35.683.566 1.15.748.353.137.882.3 1.857.344 1.054.048 1.37.058 4.041.058h.08c2.597 0 2.917-.01 3.96-.058.976-.045 1.505-.207 1.858-.344.466-.182.8-.398 1.15-.748.35-.35.566-.683.748-1.15.137-.353.3-.882.344-1.857.048-1.055.058-1.37.058-4.041v-.08c0-2.597-.01-2.917-.058-3.96-.045-.976-.207-1.505-.344-1.858a3.097 3.097 0 00-.748-1.15 3.098 3.098 0 00-1.15-.748c-.353-.137-.882-.3-1.857-.344-1.023-.047-1.351-.058-3.807-.058zM12 6.865a5.135 5.135 0 110 10.27 5.135 5.135 0 010-10.27zm0 1.802a3.333 3.333 0 100 6.666 3.333 3.333 0 000-6.666zm5.338-3.205a1.2 1.2 0 110 2.4 1.2 1.2 0 010-2.4z" clip-rule="evenodd" /></svg>
                    <span class="sr-only">Instagram page</span>
                </div>
                    
                </div>
        </div>
  </BreezeAuthenticatedLayout>
</template>

<style scoped>
.border{
    border: 3px solid #000!important;
    width: 282px;
    height: 282px;
    margin-bottom: 40px ;
}
.postagens {
    border: 2px solid white;
    width: 75%;
    height: 14%;
    position: relative;
    top: 101.3%;
    left: -1%;
    background: white;
}
.postsdarede {
    width: 91.7%;
    height: 100%;
    min-height: 335px;
    border: 3px solid rgb(0 0 0);
    margin-left: 2.9%;
    border-radius: 2px;
    position: relative;
    top: -3px;
    border-top: none;
    padding-top: 17px;
    padding-left: 7px;
    padding-right: 7px;
    padding-bottom: 14px;
}
.card{
    position: relative;
    display: flex !important;
    /* -ms-flex-direction: column; */
    flex-direction: unset;
    min-width: 0;
    word-wrap: break-word;
    background-image: linear-gradient(145deg, #000000, #2a3480);
    background-clip: border-box;
    border: 3px solid rgb(0 0 0);
    width: 853px;
    border-radius: 0.25rem;
    height: 375px;
    left: 467px;
    top: -113px;
}


.text {
  width: 79%;
  color: white;
  font-family: system-ui;
  font-size: 15px;
  font-weight: 300;

}

.borda {
  border-bottom: 3px solid rgb(0, 0, 0);
  border-left: 3px solid rgb(0, 0, 0);
  height: 107px;
  width: 408px;
  margin-left: 112px;
  padding: 7px 0px 75px 36px;
  border-top-color: rgb(0, 0, 0);
  border-right-color: rgb(0, 0, 0);
  margin-top: 0px;
}
.titulo {
  font-family: Montserrat, MAfinest;
  font-size: 3.5rem;
  margin-top: 79px;
  font-weight: 500;
  margin-left: 90px;
  line-height: 1.2;
  color: black;
}
.secondtitulo {
font-family: Montserrat, MAfinest;
    font-size: 3.5rem;
    margin-top: 79px;
    font-weight: 500;
    margin-left: 90px;
    line-height: 1.2;
    color: black;
}
.secondborda {
    border-bottom: 3px solid rgb(0, 0, 0);
    border-left: 3px solid rgb(0, 0, 0);
    height: 107px;
    width: 1092px;
    margin-left: 112px;
    padding: 7px 0px 75px 36px;
    font-family: Montserrat, MAfinest;
    font-size: 15px;
    font-weight: 300;
    border-top-color: rgb(0, 0, 0);
    border-right-color: rgb(0, 0, 0);
    margin-top: 0px;
}
.camisa {
    position: relative;
    top: -110px;
    margin-left: 109px;
}



</style>