<script setup>
import { ref } from 'vue';
let auxiliar=ref(0);
let numero=ref(0);

const kactusWOW= function(){
  auxiliar.value=numero.value;
}

const kakoso=function(plantas){
  return(auxiliar.value*plantas)
}
</script>

<template>
  <div class="text-white">
    {{ numero }} x 0 = {{kakoso(0)}}
    <br>
    {{ numero }} x 1 = {{kakoso(1)}}
    <br>
    {{ numero }} x 2 = {{kakoso(2)}}
    <br>
    {{ numero }} x 3 = {{kakoso(3)}}
    <br>
    {{ numero }} x 4 = {{kakoso(4)}}
    <br>
    {{ numero }} x 5 = {{kakoso(5)}}
    <br>
    {{ numero }} x 6 = {{kakoso(6)}}
    <br>
    {{ numero }} x 7 = {{kakoso(7)}}
    <br>
    {{ numero }} x 8 = {{kakoso(8)}}
    <br>
    {{ numero }} x 9 = {{kakoso(9)}}
    <br>
    {{ numero }} x 10 = {{kakoso(10)}}
  </div>
  
  <div class="flex">
    <h2 class="text-white">
      ingrese un numero del 1 al 10
    </h2>
    <input type="text" placeholder="Numero" class="ml-3 border-[1px] border-violet-500 rounded-lg" v-model="numero">
    <button class="p-1 ml-3 bg-red-500 rounded-lg cursor-pointer" @click="kactusWOW">enviar</button>
  </div>
</template>
