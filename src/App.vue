<script setup>
function mostrarAlert (){
  alert("Botão clicaco")
}
</script>
 
<template>
  <a v-on:click="mostrarAlert"><b>Clique aqui</b></a>

</template>
<style>
a {
  cursor: pointer;
}
</style>
