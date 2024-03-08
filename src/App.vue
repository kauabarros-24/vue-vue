<script setup>
    import { reactive } from 'vue';

    const pessoa = reactive({
        nome: 'Kauã',
        idade: 16,
        ativo: true,
    });
    function aniversario() {pessoa.idade++}
</script>
<template>
    <div>
        <p @click="aniversario()">O {{pessoa.nome}} tem {{ pessoa.idade }} anos </p>
    </div>
</template>
