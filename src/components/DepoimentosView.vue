<script setup>
import { ref } from 'vue'
import AvaliacaoView from './depoimentos/AvaliacaoView.vue';

const titulo = ref('O QUE NOSSOS CLIENTES DIZEM')

</script>

<template>
    <div class="main">
        <div class="titulo">
            <h1>{{ titulo }}</h1>
        </div>
        <AvaliacaoView />
    </div>
</template>

<style scoped>
    .main{
        border-radius: 15px;
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 35px;
        padding-bottom: 35px;
        background-color: var(--color-fundo-branco);
    }
</style>