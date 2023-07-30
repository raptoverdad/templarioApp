<template>
<div id="carouselExampleControls" class="carousel slide" data-ride="carousel" data-interval="3000">
  <div class="carousel-inner">
    <div class="carousel-item active">
      <img src="../assets/tatuajes.png" alt="Servicio 1">
      <div class="carousel-caption">

      </div>
    </div>
    <div class="carousel-item">
      <img src="../assets/perforaciones.png" alt="Servicio 2">
      <div class="carousel-caption">
   
      </div>
    </div>
    <div class="carousel-item">
      <img src="../assets/borradoLaser.png" alt="Servicio 2">
      <div class="carousel-caption">
   
      </div>
    </div>
    <!-- Agrega más elementos de carousel-item según sea necesario -->
  </div>
  <a class="carousel-control-prev" href="#carouselExampleControls" role="button" data-slide="prev">
    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
    <span class="sr-only">Anterior</span>
  </a>
  <a class="carousel-control-next" href="#carouselExampleControls" role="button" data-slide="next">
    <span class="carousel-control-next-icon" aria-hidden="true"></span>
    <span class="sr-only">Siguiente</span>
  </a>
</div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'carrusel',
  components: {
   
  }
}
</script>
<style scoped>
.carousel{
    height: min-content;
    width: 100vw;
border: 3PX SOLID BLACK;
overflow: hidden;
}
img{
  width: 1080px;
  height: 576px;
  z-index: 1;
}
@media(max-width:1024px){
    img{
width:854px;
height:480px;
}
}
@media(max-width:900px){
    img{
        width:320px;
height:180px;
}

}
@media(max-width:650px){
img{
width:320px;
height:180px;
}
}
</style>
