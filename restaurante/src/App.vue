<!-- <script setup>

import { ref } from 'vue';
let index = ref(1)
let restauranteUniversitario = ref([
    {
      dia:'lunes',
      desayuno: ['Arepa de Huevo', 'Empanada', 'Patacon'],
      almuerzo: ['Mondongo', 'Bandeja Paisa', 'Changua'],
      cena: ['Hamburguesa', 'Salchipapa', 'Hot-Dog']
          },
  {
    dia:'martes',
  desayuno: ['Arepa con huevo', 'Pan con queso', 'Croissant'],
  almuerzo:['Meesi', 'Antonio', 'xd'],
  cena:['uwu', 'onixan', 'quehacesxd']
},
{
  dia:'miercoles',
  desayuno:['tamal', 'buñuelos', 'natilla'],
  almuerzo:['Hamburguesa', 'Salchipapa', 'Hot-Dog'],
  cena: ['pechuga', 'carne', 'lomo']
},
{
  dia:'jueves',
  desayuno: ['yuca', 'chicharron', 'pasta'],
  almuerzo: ['lechona', 'salchichon', 'tamal'],
  cena:['papa', 'xd', 'uwu']
},
{
  dia:'viernes',
  desayuno:['suero', 'queso', 'mantequilla'],
  almuerzo: ['chorizo', 'fritanga', 'pescado'],
  cena: ['xd', 'xd', 'xd'],
},
{
dia:'sabado',
desayuno: ['manzana', 'pera', 'mandarina'],
almuerzo: ['morcilla', 'arroz', 'pasta'],
cena: ['no hay cenas']
}])

function doclick(indice){
  index.value = indice
}

function xd (i){
  restauranteUniversitario.value.desayuno[index] = i
}



</script>

<template>

  <div class="text-3xl font-bold flex justify-center">
    <h1 class="">RESTAURANTE UNIVERSITARIO</h1>
  </div>

<div class="flex justify-between max-w-xs mx-auto mt-20">

<div class="grid grid-rows-6 p-4">

<div @click="doclick(0)" class="bg-gray-300 w-40 h-8 mt-2 text-center text-xl hover:bg-blue-300">Lunes</div>
<div @click="doclick(1)" class="bg-gray-300 w-40 h-8 mt-2 text-center text-xl hover:bg-blue-300">Martes</div>
<div @click="doclick(2)" class="bg-gray-300 w-40 h-8 mt-2 text-center text-xl hover:bg-blue-300">Miercoles</div>
<div @click="doclick(3)"  class="bg-gray-300 w-40 h-8 mt-2 text-center text-xl hover:bg-blue-300">Jueves</div>
<div @click="doclick(4)"  class="bg-gray-300 w-40 h-8 mt-2 text-center text-xl hover:bg-blue-300">Viernes</div>
<div @click="doclick(5)" class="bg-gray-300 w-40 h-8 mt-2 text-center text-xl hover:bg-blue-300">Sabado</div>

</div>

<div class="bg-blue-300">
<div class="flex gap-10 p-4" >
  <div @click="xd(0)" class="text-xl text-white font-light">Desayuno</div>
  <div  class="text-xl text-white font-light">Almuerzo</div>
  <div  class="text-xl text-white font-light">Cena</div>
</div>
<div>
 <div class="">
    <div class="mt-4" v-for="(obj, xd ) in restauranteUniversitario[index].desayuno" :key="xd"> Desayunos: {{ obj }}</div>
    <div class="mt-4" v-for="(obj, xd) in restauranteUniversitario[index].almuerzo" :key="xd"> Almuerzo: {{ obj }}</div>
    <div class="mt-4" v-for="(obj, xd) in restauranteUniversitario[index].cena" :key="xd">Cena: {{ obj }}</div>
  </div>
 
</div>
</div>
</div>
  
</template>

 -->

 <script setup>
  import { ref } from 'vue';

  let indice=ref(0)
  let pepe=ref(0)
  let restaurante= ref([
    {
      dia:'lunes',
      desayuno: ['Arepa de Huevo', 'Empanada', 'Patacon'],
      almuerzo: ['Mondongo', 'Bandeja Paisa', 'Changua'],
      cena: ['Hamburguesa', 'Salchipapa', 'Hot-Dog']
          },
  {
    dia:'martes',
  desayuno: ['Arepa con huevo', 'Pan con queso', 'Croissant'],
  almuerzo:['Meesi', 'Antonio', 'xd'],
  cena:['uwu', 'onixan', 'quehacesxd']
},
{
  dia:'miercoles',
  desayuno:['tamal', 'buÃ±uelos', 'natilla'],
  almuerzo:['Hamburguesa', 'Salchipapa', 'Hot-Dog'],
  cena: ['pechuga', 'carne', 'lomo']
},
{
  dia:'jueves',
  desayuno: ['yuca', 'chicharron', 'pasta'],
  almuerzo: ['lechona', 'salchichon', 'tamal'],
  cena:['papa', 'xd', 'uwu']
},
{
  dia:'viernes',
  desayuno:['suero', 'queso', 'mantequilla'],
  almuerzo: ['chorizo', 'fritanga', 'pescado'],
  cena: ['xd', 'xd', 'xd'],
},
{
dia:'sabado',
  desayuno: ['manzana', 'pera', 'mandarina'],
  almuerzo: ['morcilla', 'arroz', 'pasta'],
  cena: ['no hay cenas']
}])

 

    function ver(i){
      indice.value=i
    }
    function escoger(i){
      pepe.value=i
    }
</script>

<template>
 <h1 class="bg-gray-500 text-center font-medium uppercase text-4xl ">restaurante universitario </h1>
  <div class=" mt-6 flex justify-center w-[50%] mx-auto">
    <div class="w-[30%]">
      <div v-for="(obj,i) in restaurante" :key="i" class="" @click="ver(i)">
        <div v-if="indice==i" class="bg-sky-400 mt-2 py-1 px-2">{{ restaurante[i].dia }}</div>
        <div v-else class="bg-gray-500/30 mt-2 px-2 py-1">{{ restaurante[i].dia }}</div>
      </div>
    </div>
    <div class="w-[70%] bg-sky-400 mt-2">
      <div class="flex gap-5  ml-8">
        <p @click="escoger(0)" v-if="pepe==0" class="cursor-pointer p-1 bg-sky-700/80">Desayuno</p>
        <p @click="escoger(0)" v-else class="cursor-pointer p-1 ">Desayuno</p>
        <p @click="escoger(1)" v-if="pepe==1" class="cursor-pointer p-1 bg-sky-700/80">Almuerzo</p>
        <p @click="escoger(1)" v-else class="cursor-pointer p-1 ">Almuerzo</p>
        <p @click="escoger(2)" v-if="pepe==2" class="cursor-pointer p-1 bg-sky-700/80">Cena</p>
        <p @click="escoger(2)" v-else class="cursor-pointer p-1 ">Cena</p>
        
      </div>
      <ul v-for="(obj,i) in restaurante[indice].desayuno" :key="i" class="ml-4">
        <li v-if="pepe==0">
          {{ restaurante[indice].desayuno[i] }}
        </li>
        <li v-else-if="pepe==1">
          {{ restaurante[indice].almuerzo[i] }}
        </li>
        <li v-else>
          {{ restaurante[indice].cena[i] }}
        </li>
      </ul>
      
    </div>
  
  </div>
</template>

<style scoped>
</style>
