<template>
   <div id="carouselExampleFade" class="carousel slide carousel-fade position" data-bs-ride="carousel">
  <div class="carousel-inner">
    <div class="carousel-item active " data-bs-interval="3000">
      <img src="img/jopegroup.jpg" class="d-block w-100" alt="..." style="border-radius: 4px;">
    </div>
    <div class="carousel-item " data-bs-interval="3000">
      <img src="img/jopeestrada.jpg" class="d-block w-100" alt="..." style="border-radius: 4px;">
    </div>
    <div class="carousel-item " data-bs-interval="3000">
      <img src="img/jopebanner.jpg" class="d-block w-100" alt="..." style="border-radius: 4px;">
    </div>
  </div>
  <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleFade" data-bs-slide="prev">
    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
    
  </button>
  <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleFade" data-bs-slide="next">
    <span class="carousel-control-next-icon" aria-hidden="true"></span>
    
  </button>
</div>
</template>
<script>

</script>
<style scoped>
.position{
    max-width: 800px; 
    position: sticky;
}
@media only screen and (max-width: 414px){
        .w-100{
            width: 87%!important; 
        }
        .carousel-control-next {
        right: 42px !important;
    }
    .carousel-control-prev {
        left: -12px !important;
    }
}
@media only screen and (max-width: 1025px){
        .position{
            margin-left: 68px;
        }
}
</style>