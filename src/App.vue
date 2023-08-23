<!-- single file component -->
<script setup>
const name = "Vue dinamico";
const styleColor = "color:blue";
const arrayColores = ["blue","red","peru"];
const activo = true;
</script>

<template>
  <h1>comienzo del proyecto {{ name.toUpperCase() }}</h1>
  <!-- v-bind es igual a solo poner : -->
  <h2 v-bind:style="styleColor">soy azul owo </h2>
  <h2>{{ arrayColores }}</h2>
  <h2 :style="`color: ${arrayColores[1]}`">soy azul owo </h2>
  <h2>{{ activo ? 'estoy activo' : 'estoy inactivo' }} </h2>
  <p></p>
</template> 

<style>
h1 {
  color:aqua;
}
</style>