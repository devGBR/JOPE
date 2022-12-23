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
                <div class="postsdarede"></div>
        </div>
  </BreezeAuthenticatedLayout>
</template>

<style scoped>

.postsdarede {
    width: 91.7%;;
    height: 320px;
    border: 3px solid rgb(0 0 0);
    margin-left: 2.9%;
    border-radius: 2px;
    position: relative;
    top: -3px;
    border-top: none;
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