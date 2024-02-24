
<script setup>
const mensagem = 'programar'
function reverter(texto) {
  return texto.split('').reverse('').join('')
}
</script>
 
<template>
  <p>{{ reverter(mensagem) }}</p>
  

</template>


<style scoped>
</style>