
<script setup>
import { createSlots, ref } from "vue";
const count = ref(0);

const addToCount = () =>{
  count.value = count.value + 1
}
const substractFormCount = () =>{
  count.value = count.value - 1
}
</script>


<template>
  <main>
    <div class="card">
      <h3>The Current Counter is...</h3>
      <h1>{{ count }}</h1>
      <button class="botonrestar" @click="substractFormCount()">-</button>
      <button class="botonsumar" @click="addToCount()">+</button>
    </div>
  </main>
</template>

<style>
.main{
  background-color: rgb(24, 24, 78);
}
.card {
  width: 300px;
  margin: auto;
  padding: 20px;
  text-align: center;
  border-radius: 25px;
  background-color: #acacac75; /* Fondo gris claro */
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1); /* Sombra sutil */
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
}

.card h2 {
  margin-bottom: 10px;
  color: #333;
}

.card p {
  font-size: 24px;
  font-weight: bold;
  margin: 10px 0;
  color: #10dd3d; /* Azul llamativo */
}

.card button {
  margin: 5px;
  padding: 10px 15px;
  border: none;
  border-radius: 5px;
  color: white;
  font-size: 16px;
  cursor: pointer;
  
}

.card button:hover {
  background-color: #abb1ab; /* Azul más oscuro */
}

.botonsumar{
background-color: green;
}
.botonrestar{
background-color: red;
}





</style>