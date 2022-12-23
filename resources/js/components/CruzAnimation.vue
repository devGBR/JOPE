<template>
    <div class="cruz">
      <div class="horizontal"></div>
      <div class="vertical"></div>
      <div :class="VerAnim" class="principal">
        <div class="versiculo">
          “Porque Deus amou o mundo de tal maneira,<br />
          que deu o seu Filho Unigênito, para que todo a<br />
          quele que nele crê não pereça, <br />
          mas tenha a vida eterna” <br />
          (João 3:16).
        </div>
      </div>
    </div>
</template>
<script>
export default {
    data() {
    return {
      time: true,
      VerAnim: "PrimaryAnim",
    };
  },
  mounted() {
    setTimeout(() => {
      this.VerAnim = "SecondAnim";
    }, 4000);

    if (this.time === true) {
      setTimeout(() => {
        this.time = false;
      }, 10000);
    }
  },
}
</script>
<style scoped>
.principal {
  position: relative;
  width: 328px;
  left: 0px;
  top: 0px;
}
.horizontal {
  border: 8px solid rgb(255, 255, 255);
  background: rgb(162, 10, 10);
  width: 120px;
  height: 18px;
  position: relative;
  left: 97px;
  top: 50px;
  /* animation: hrt 2s; */
  animation: pulo 4s infinite;
}
.vertical {
  border: 8px solid rgb(255, 255, 255);
  background: rgb(141, 19, 19);
  width: 20px;
  height: 144px;
  position: relative;
  left: 149px;
  /* top: 0px; */
  /* animation: vrt 2s; */
  animation: pulo1 4s infinite;
}
.cruz {
  position: absolute;
  left: 6px;
  top: 150px;
  width: 331px;
  height: 300px;
}
.versiculo {
  font-family: Baskerville;
  font-size: 17.5px;
  color: white;
  text-shadow: -1px -1px 0px rgb(17, 17, 17), -1px 1px 0px rgb(18, 17, 17),
    1px -1px 0px rgb(21, 21, 21), 1px 0px 0px rgb(20, 20, 20);
}
.PrimaryAnim {
  animation: PrimaryAnim 4s;
}
.SecondAnim {
  animation: SecondAnim 4s infinite;
}
@media only screen and (max-width: 1025px) {
  .cruz {
    left: 68px;
    top: 150px;
  }
}
@keyframes SecondAnim {
  0% {
    top: 6px;
  }
  50% {
    top: -47px;
  }
  100% {
    top: 6px;
  }
}
@keyframes PrimaryAnim {
  0% {
    position: relative;
    opacity: 0;
  }
  30% {
    opacity: 0.2;
  }
  100% {
    position: relative;

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
  0% {
    /* top: 183px; */
    top: 0px;
  }
  50% {
    top: -50px;
  }
  100% {
    top: 0px;
  }
}
</style>