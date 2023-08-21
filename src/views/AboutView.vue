<template>
<section>
  
  <h3>Estamos ubicados en condominio don gaston
Ing. Lloyd 01741
8500055 Quinta Normal
Región Metropolitana, Chile</h3>
  <div id="map"></div>
</section>

</template>

<script>
// @ is an alias to /src


export default {
  name: 'about',
  components: {

  }, 
  mounted(){
 this.iniciarMap()
  },methods:{
    iniciarMap(){
    var coord = {lat:-33.4290889 ,lng: -70.7049088};
    var map = new google.maps.Map(document.getElementById('map'),{
      zoom: 10,
      center: coord
    });
    var marker = new google.maps.Marker({
      position: coord,
      map: map
    });
}
  }
}
</script>
<style scoped>
#map{
 border: 2px solid #f00;
  width: 50vh;
  height: 50vh;
}
section{
  display: flex;
  width: 100vw;
  height: 60vh;
  justify-content: center;
  align-items: center;
}
h3{
  width: 50vw;
}
@media(max-width:900px){
  #map{
  width: 90vw;
  height: 50vh;
}
  h3{
    width: 90vw;
  }
  section{
  flex-direction: column;
  height: min-content;
  padding-bottom: 6vh;
}
}
</style>