<script setup>
  import { ref } from 'vue';
  import boton from './components/boton.vue';
  import imagen1 from './assets/imagenes/mechanichus.jpg';
  import imagen2 from './assets/imagenes/piedra.jpg';
  import imagen from './components/imagen.vue';
  const mostrarImagen1 = ref(false);
  const mostrarImagen2 = ref(false);
  const mostrarImagen3 = ref(false);

  const toggleImagen1 = () => mostrarImagen1.value = !mostrarImagen1.value;
  const toggleImagen2 = () => mostrarImagen2.value = !mostrarImagen2.value;
  const toggleImagen3 = () => mostrarImagen3.value = !mostrarImagen3.value;
</script>

<template>
  <boton @clickBoton="toggleImagen1" texto="fuck"/>
  <br>
  <img :src="imagen1" alt="imagen1" v-if="mostrarImagen1">
  <br>
  <boton @clickBoton="toggleImagen2" texto="you"/>
  <br>
  <img :src="imagen2" alt="imagen" v-show="mostrarImagen2">
  <br>
  <boton @clickBoton="toggleImagen3" texto="human"/>
  <br>
  <imagen v-if="mostrarImagen3"/>
</template>

<style scoped>

</style>
