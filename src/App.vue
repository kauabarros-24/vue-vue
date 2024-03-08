<script setup>
    import { ref} from 'vue';
    const contador = ref(0);
    const contador1 = ref(0)
    function incrementar() {contador.value++;}
    function decrementar() {if (contador.value >= 0) {contador.value--;}}
    function incrementar2() {contador1.value++;}
    function decrementar2() {if (contador1.value >= 0){contador1.value--;}}
    const soma = contador1 + contador;
    function resposta() {(soma % 2 == 0) ? document.write('O valor é par') : document.write('O valor é ímpar');}
    const booleana = true;
    function testeBoolean(){(booleana == true) ? document.write("Verdadeiro") : document.write("Falso")}

</script>
<template>
    <div>
        <p> {{ contador + contador1}}</p>
        <button @click="incrementar">Clique para incrementar o primeiro valor</button>
        <button @click="decrementar">Clique para decrementar o primeiro valor </button>
        <button @click="incrementar2">Clique para incrementar o primeiro valor</button>
        <button @click="decrementar2">Clique para decrementar o primeiro valor </button>
        <div v-if="soma > 10 || soma < 10">A sua soma excedeu ou precedeu o valor 10</div>
        <div v-bind="resposta"></div>
        <div v-bind="testeBoolean"></div>    
    </div>

</template>




 