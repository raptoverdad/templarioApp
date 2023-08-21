<template>

 <div class="modal" v-if="$store.state.modalAbierto==true">
    <img class="modalImg" :src="fotoClickeada" alt="Templario-tatto-studio">
    <button v-on:click="cerrarModal()">Volver</button>
 </div>

  <div class="gallery">
    <div v-for="(image, index) in images" :key="index" class="fade" ref="imageElements">
      <img class="click" :src="image" v-on:click="abrirModal(image)"/>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      images: [
        'https://res.cloudinary.com/debvhmcid/image/upload/v1692592508/templario/Captura8_bdr8yw.jpg',
        'https://res.cloudinary.com/debvhmcid/image/upload/v1692592508/templario/Captura6_gu9t5h.jpg',
        'https://res.cloudinary.com/debvhmcid/image/upload/v1692592508/templario/Captura2_yg0o1j.jpg',
        'https://res.cloudinary.com/debvhmcid/image/upload/v1692592508/templario/Captura5_mxhgba.jpg',
        'https://res.cloudinary.com/debvhmcid/image/upload/v1692592508/templario/Captura_lsy45l.jpg',

        'https://res.cloudinary.com/debvhmcid/image/upload/v1692598802/templario/Captura18_dcy5kj.jpg',
        'https://res.cloudinary.com/debvhmcid/image/upload/v1692598802/templario/Captura20_qpbxxv.jpg',
        'https://res.cloudinary.com/debvhmcid/image/upload/v1692598802/templario/Captura19_hp2okj.jpg',
        'https://res.cloudinary.com/debvhmcid/image/upload/v1692598802/templario/Captura15_y9mukd.jpg',
        'https://res.cloudinary.com/debvhmcid/image/upload/v1692598803/templario/Captura23_bcvmdd.jpg',

        'https://res.cloudinary.com/debvhmcid/image/upload/v1692598802/templario/Captura17_dcb7hm.jpg',
        'https://res.cloudinary.com/debvhmcid/image/upload/v1692598803/templario/Captura22_zjpq59.jpg',
        'https://res.cloudinary.com/debvhmcid/image/upload/v1692598803/templario/Captura21_bjaart.jpg',
        'https://res.cloudinary.com/debvhmcid/image/upload/v1692598802/templario/Captura16_on9ztc.jpg',
        'https://res.cloudinary.com/debvhmcid/image/upload/v1692598802/templario/Captura13_qcvdqa.jpg',


        'https://res.cloudinary.com/debvhmcid/image/upload/v1692598802/templario/Captura9_cqotsm.jpg',
        'https://res.cloudinary.com/debvhmcid/image/upload/v1692598802/templario/Captura11_mksqh9.jpg',
        'https://res.cloudinary.com/debvhmcid/image/upload/v1692598802/templario/Captura14_ghenmx.jpg',
        'https://res.cloudinary.com/debvhmcid/image/upload/v1692598802/templario/Captura10_cikcm2.jpg',
        'https://res.cloudinary.com/debvhmcid/image/upload/v1692598802/templario/Captura12_pjnar7.jpg',

      ], // Tus URLs de imágenes aquí
      isVisible: [],
      fotoClickeada:''
    };
  },
  mounted() {
    const options = {
      root: null, // Use viewport como el root
      rootMargin: '0px', // Sin margen adicional
      threshold: 0.5 // 50% de intersección requerida
    };

    const observer = new IntersectionObserver(this.callback, options);

    const fadeElements = this.$refs.imageElements;
    fadeElements.forEach(element => {
      observer.observe(element);
    });
  },
  methods: {
    callback(entries, observer) {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          entry.target.classList.add('show'); // Agrega la clase show al elemento
        }
      });
    },
    cerrarModal(){
      this.$store.fotoClickeada=""
    this.$store.state.modalAbierto=false
   
  },abrirModal(src){
    this.fotoClickeada=src
    this.$store.state.modalAbierto=true
  }
  },
};
</script>

<style scoped>
/* Estilos para la galería */
.modal{
        display:flex;
        justify-content:center;
        flex-direction:column;
        align-items:center;
        position:fixed;
        z-index:100;
        left:0;
        top:0;
        width:100vw;
        height:100vh;
        background-color:rgba(0, 0, 0, 0.85);
        display:flex;
        font-family: 'Poppins', sans-serif;
        text-align:center;
        font-size:3vh;
  
      }
      .modalImg{
        height: 700px;
        width: 700px;
      }
   
.gallery {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  grid-gap: 10px;
  justify-items: center; /* Centra horizontalmente los elementos */
  width: 80vw;
}

.fade {
  opacity: 0;
  transition: opacity 0.5s; /* Cambia la propiedad de transición */
}

.show {
  opacity: 1; /* Cambia la clase a mostrar la opacidad completa */
}

.click {
  width: 100%;
  height: auto;
  border-radius: 5px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  cursor: pointer;
}
@media (max-width: 1000px) {
  .gallery {
    grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
  }
  .modalImg{
        height: 600px;
        width: 600px;
      }
   
}
@media (max-width: 700px) {
  .gallery {
    grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
  }
  .modalImg{
        height: 500px;
        width: 500px;
      }
   
}
@media (max-width:500px) {
  .gallery {
    grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
  }
  .modalImg{
        height: 400px;
        width: 400px;
      }
   
}
@media (max-width:400px) {
  .gallery {
    grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
  }
  .modalImg{
        height: 300px;
        width: 300px;
      }
   
}
</style>