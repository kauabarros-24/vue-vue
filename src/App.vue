<script setup>
import { ref } from 'vue' 
const contador = ref(0)

function decrementar() {
  contador.value--
}
</script>
 
<template>
  <button @click="contador++">+</button>
  <button @click="decrementar()">-</button>
  
  <p>Valor contador: {{ contador }}</p>
</template>


<style scoped></style>