<!-- single file component -->
<script setup>
const name = "Vue dinamico";
const styleColor = "color:blue";
const arrayColores = ["blue","red","peru"];
const activo = true;
const activo2 = false;
const arrayFrutas = ["🍎", "🍌", "🍉", "🍓", "🍒"];
const arrayFrutas2 = [
        {
            name: "Manzana",
            price: "$1.00",
            description: "Una manzana",
        },
        {
            name: "Pera",
            price: "$2.00",
            description: "Una pera",
        },
        {
            name: "Naranja",
            price: "$3.00",
            description: "Una naranja",
        },
    ];
/*
const fruta = {
        name: "Naranja",
        price: "$3.00",
        description: "Una naranja",
    };
  */
  const arrayFrutas3 = [
    {
        name: "Manzana",
        price: "$1.00",
        description: "Una manzana",
        stock: 0,
    },
    {
        name: "Pera",
        price: "$2.00",
        description: "Una pera",
        stock: 10,
    },
    {
        name: "Naranja",
        price: "$3.00",
        description: "Una naranja",
        stock: 20,
    },
];
const handleClick = () => {
        console.log("me diste cick");
    };

    const handleClick2 = (message) => {
        console.log(message);
    };

let counter = 0;

const increment2 = () => {
    counter++;
    // efectivamente aumentar
    console.log(counter);
};

//increment reactive 
import {ref} from "vue";
const counter2 = ref(0);

const increment = () => {
    counter2.value++;
};

</script>

<template>
    <h1>comienzo del proyecto {{ name.toUpperCase() }}</h1>

 <!-- 
  <h1>comienzo del proyecto {{ name.toUpperCase() }}</h1>
  // v-bind es igual a solo poner : 
  <h2 v-bind:style="styleColor">soy azul owo </h2>
  <h2>{{ arrayColores }}</h2>
  <h2 :style="`color: ${arrayColores[1]}`">soy azul owo </h2>
  <h2>{{ activo ? 'estoy activo' : 'estoy inactivo' }} </h2>
  <p v-if="activo === true">estoy activo</p>
  <p v-else-if="activo === false">estoy inactivo</p>
  <p v-else>estoy indeciso xdxd</p>
  <h2 v-show="activo2">estoy inactivo v-show</h2>
 -->

 <!--
  // v-for arrays
  <ul>
        <li v-for="(fruta, index) in arrayFrutas" :key="index">
            {{ fruta }}
        </li>
  </ul> 
  
  <ul>
        <li v-for="fruta in arrayFrutas2" :key="name">
            {{ fruta.name }} - {{ fruta.price }} - {{ fruta.description }}
        </li>
    </ul>
  -->

  <!-- objetos -->
  <!--
  <ul>
        <li v-for="(value, propiedad) in fruta">
            {{ propiedad }} : {{ value }}
        </li>
    </ul>
  -->
  <!-- v-if v-for juntos -->
  <!--
  <ul>
    <template v-for="fruta in arrayFrutas3" :key="fruta.name">
        <li v-if="fruta.stock > 0">
            {{ fruta }}
        </li>
    </template>
  </ul>
-->
  <!--EVENTOS  V-OP O @-->
  <h1>Hola {{ name }}!</h1>
    <button v-on:click="handleClick">Click aquí</button>
    <button @click="handleClick">Click aquí</button>
    <button @click="handleClick('Mensaje desde botón')">Click aquí</button>
    <button @click.right.prevent="handleClick('Mensaje desde botón')">
    Click right
</button>
<button @click.middle="handleClick('Mensaje desde botón')">
    Click middle
</button>

<h2>{{ counter }}</h2>
<button @click="increment2">Click incremet</button>

<h2>{{ counter2 }}</h2>
    <button @click="increment">Click incremet</button>





</template> 

<style>
h1 {
  color:aqua;
}
</style>