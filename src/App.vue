<template>
  <nav>
    <img alt="templario tatto studio logo" src="@/assets/TEMPLARIO.png">
    <div class="routes">
      <router-link to="/">Inicio</router-link> |
      <router-link to="/about">Contacto</router-link>
    </div>
  </nav>
  <a href="https://api.whatsapp.com/send?phone=56947742842" target="_blank"><img class="whatsappLink" src="./assets/whatsapp.png" alt=""></a>
  <router-view/>
</template>

<style>

.whatsappLink{
  position: fixed;
  right: 5vh;
  border-radius: 100%;
  bottom:5vh;
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
