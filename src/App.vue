<template>
  <nav>
    <img alt="templario tatto studio logo" src="@/assets/TEMPLARIO.png">
    <div class="routes">
      <router-link to="/">Inicio</router-link>
      <router-link to="/ubicacion">Ubicación</router-link>
    </div>
  </nav>
  <a href="https://api.whatsapp.com/send?phone=56963723135" target="_blank"><img class="whatsappLink" src="./assets/whatsappoficial.png" alt=""></a>
<div v-on:click="redirectToInstagram" class="footer"><img class="instagram" src="@/assets/instagram.jpg"></div>
  <router-view/>
</template>
<script>

export default {
  name: 'HomeView',
  components: {
  
  },methods:{
    redirectToInstagram() {
      window.location.href = 'https://www.instagram.com/templario_tattoo_studio/';
    }
  }
}
</script>
<style>
.instagram{
height:5vh ;
width: 5vh;
}
.whatsappLink{
  position: fixed;
  right: 2vw;
  bottom:7vh;
  z-index: 3;
  height:10vh ;
width: 10vh;
}
.footer{
position:fixed;
left:0;
bottom:0;
background-color:#000;
display:flex;
justify-content:center;
align-items:center;
height: 6vh;
width: 100%;
z-index: 2;
cursor: pointer;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
img{
  height: 24vh;
  width: 24vh;
}
nav {
  width: 100%;
  max-width: 100%;
  height: 30vh;
  background-color: black;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  overflow: hidden;
}
.routes{
  width: 100vw;
  height: 4vh;
  display: flex;
  justify-content: center;
  align-items: center;
}
nav a {
  font-weight: bold;
  color: #fff;
  margin: 0px 10px;
}

nav a.router-link-exact-active {
  color: #f00;
}
</style>
