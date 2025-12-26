<script setup>
import CabecalhoView from '@/components/home/CabecalhoView.vue'
</script>

<template>
    <div class="main">
        <CabecalhoView />
    </div>
</template>

<style scoped>
    .main{
        background-color: var(--color-preto);
        height: 100dvh;
        width: 100dvw;
        position: relative;
        z-index: 1;
    }

    .main::before{
        content: "";
        background-image: url('/src/assets/img/home/pagina_home.png');
        background-repeat: no-repeat;
        background-size: cover;
        background-position: center top;
        position: absolute;
        top: 0;
        left: 0;
        height: 100%;
        width: 100%;
        opacity: 0.5;
        z-index: -1;
    }

    @media screen and (max-width: 500px) {
        .main::before{
            background-position: 68% top;
        }
    }
</style>