<script setup>
import PrincipalView from '@/components/PrincipalView.vue';
import ChamadaView from './components/ChamadaView.vue';
import ServicosView from './components/ServicosView.vue';
import SegurancaView from './components/SegurancaView.vue';
import EscolhaView from './components/EscolhaView.vue';
import DepoimentosView from './components/DepoimentosView.vue';


</script>

<template>
  <div class="container">
    <section id="inicio">
      <PrincipalView />
    </section>

    <section id="servicos">
      <ServicosView />
    </section>

    <section id="depoimentos">
      <DepoimentosView />
    </section>

    <section id="seguranca">
      <SegurancaView />
    </section>

    <section class="escolha">
      <EscolhaView />
    </section>

    <section id="contato">
      <ChamadaView />
    </section>
  </div>

</template>

<style scoped>
  .container{
    display: flex;
    flex-direction: column;
    gap: 25px;
    padding: clamp(12px, 3vw, 16px);
    background-color: var(--color-branco);
  }
  #inicio{
    flex: 1;
  }
</style>
