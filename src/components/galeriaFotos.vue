<template>
      <div class="gallery">
    <img src="../assets/logo.png" alt="Imagen 1">
    <img src="../assets/logo.png" alt="Imagen 2">
    <img src="../assets/logo.png" alt="Imagen 3">
    <img src="../assets/logo.png" alt="Imagen 1">
    <img src="../assets/logo.png" alt="Imagen 2">
    <img src="../assets/logo.png" alt="Imagen 3">
    <img src="../assets/logo.png" alt="Imagen 1">
    <img src="../assets/logo.png" alt="Imagen 2">
    <img src="../assets/logo.png" alt="Imagen 3">
    <img src="../assets/logo.png" alt="Imagen 1">
    <img src="../assets/logo.png" alt="Imagen 2">
    <img src="../assets/logo.png" alt="Imagen 3">
    <img src="../assets/logo.png" alt="Imagen 2">
    <img src="../assets/logo.png" alt="Imagen 3">
    <!-- Agrega más imágenes según sea necesario -->
  </div>

  </template>
  
  <script>
  // @ is an alias to /src

  export default {
    name: 'galeriaFotos',
    components: {
     
    }
  }
  </script>
<style>
/* Estilos para la galería */

.gallery {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  grid-template-rows: repeat(2,25vh);
  gap: 10px;
}

.gallery img {
  width: 100%;
  height: auto;
  border-radius: 5px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}
@media (max-width: 768px) {
  .gallery {
    grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
  }
}
</style>
