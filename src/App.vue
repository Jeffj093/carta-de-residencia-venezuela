<script setup>
import HelloWorld from './components/HelloWorld.vue'
import Formulario from './components/formulario.vue';
</script>

<template>
  <div>
    <a href="https://vuejs.org/" target="_blank">
      <img src="src\assets\lemon-squash.svg" class="logo vue" alt="Vue logo" />
    </a>
  </div>
  
  <Formulario />
  <HelloWorld msg=" Generador de Documentos Bancarios" />
  
  
</template>

<style scoped>
.logo {
  height: 15em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
