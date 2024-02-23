<script>
/**export default {
  data() {
    return {
      contador: 0

    }
  },
  methods: {
    incrementarContador() {
      this.contador++
    },
    decrementarContador() {
      if (this.contador > 0) {this.contador--}
      else {this.contador = 0}
    }
  },
  mounted() {
    console.log(`O valor do contador inicial é ${this.contador}`)
  }
}
**/
</script>
<script setup>
import { ref, onMounted } from 'vue'
const contador = ref(0)
function incrementarContador() {contador.value++}
function decrementarContador() {
  if (contador.value > 0) contador.value-- 
  else contador.value = 0
}
function resetar() {
  if (contador.value >= 1) {
    contador.value = 0

  }
}
onMounted(() => {
  console.log(`Contador incrementado: ${contador.value}`)
  }

)
</script>
 
<template>
  <button @click="incrementarContador">+</button>
  <button @click="decrementarContador">-</button>
  <button @click="resetar">Resetar</button>
  
  <p>Valor contador: {{ contador }}</p>
</template>


<style scoped>
</style>