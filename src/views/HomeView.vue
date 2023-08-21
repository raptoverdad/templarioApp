<template>
  <div class="home">
      <h1>Nuestros servicios</h1>
 
        <carrusel></carrusel>
    
      <h1>Nuestro trabajo</h1>
   
        <galeriaFotos></galeriaFotos>
     
   
  </div>
</template>

<script>
// @ is an alias to /src
import vistaPredeterminada from '@/components/vistaPredeterminada.vue'
import galeriaFotos from '@/components/galeriaFotos.vue'
import seccion from '@/components/seccion.vue'
import carrusel from '@/components/carrusel.vue'

export default {
  name: 'HomeView',
  components: {
    vistaPredeterminada,
    galeriaFotos,
    seccion,
    carrusel
  }
}
</script>
<style scoped>
h1{
  font-size:7vh;
  border-bottom: 4px solid black;
 padding-top:2%;
  width: 80vw;
}
.home{
  height: min-content;
  width: 100%;
  margin: 0;
  padding: 0;
  overflow: hidden;
  padding-bottom: 6vh;
  display: flex;
  flex-direction: column;
justify-content: center;
align-items: center;
}
@media(max-width:650px){
  h1{
  font-size:5vh;

}
}
</style>