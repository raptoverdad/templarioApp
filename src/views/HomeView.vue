<template>
  <div class="home">
    <carrusel></carrusel>
    <galeriaFotos></galeriaFotos>
    <seccion tittle="Hola mundo"></seccion>
  
    
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

.home{
  height: 75vh;
  width: 100%;
  margin: 0;
  padding: 0;
  overflow: hidden;
}
</style>