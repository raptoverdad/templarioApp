<template>
    <section>
      <h1>{{ tittle }}</h1>
    </section>
</template>
<script>
// @ is an alias to /src

export default {
  name: 'seccion',
  props: {
    tittle: String
  },
  components: {
   
  }
}
</script>
<style>
/* Estilos para la galería */
section{
width: 100%;
max-width: 100%;
height: min-content;
}

</style>
