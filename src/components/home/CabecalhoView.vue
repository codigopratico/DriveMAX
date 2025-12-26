<script setup>
import { ref } from 'vue'


const link_1 = ref('Início')
const link_2 = ref('Serviços')
const link_3 = ref('Depoimentos')
const link_4 = ref('Como Funciona')
const link_5 = ref('Contato')
const btn = ref('Agendar Consultoria')

const responsivo = ref(false)

const toggle = () => {
    responsivo.value = !responsivo.value
}
</script>

<template>
    <header class="cabecalho">
        <div class="logo">
            <img src="../../assets/img/logo.png" alt="">
            <div class="icone_menu">
            <i class="bi bi-list" 
            @click="toggle" 
            v-show="!responsivo"></i>

            <i class="bi bi-x-lg"
            @click="toggle"
            v-show="responsivo"></i>
        </div>
        </div>
        <div :class="{navigation: !responsivo, menu: responsivo}">
            <nav class="links">
                <a href="#">{{ link_1 }}</a>
                <a href="#">{{ link_2 }}</a>
                <a href="#">{{ link_3 }}</a>
                <a href="#">{{ link_4 }}</a>
                <a href="#">{{ link_5 }}</a>
            </nav>
            <div class="butao">
                <button>{{ btn }}</button>
            </div>
        </div>
    </header>
</template>

<style scoped>
    .cabecalho{
        background: transparent;
        display: flex;
        align-items: center;
        justify-content: space-between;
        height: 90px;
        padding: 0 25px;
        top: 0;
        position: absolute;
        width: 100%;
        z-index: 2;
    }
    .navigation{
        display: flex;
        align-items: center;
        gap: 12px;
    }
    .icone_menu{
        display: none;
    }.logo{
        display: flex;
        align-items: center;
        justify-content: space-between;
    }
    .logo img{
        height: var(--img-logo);
        box-shadow: 0 4px 20px rgba(255, 255, 255, 0.02);
    }
    .links{
        display: flex;
        gap: 12px;
    }.links a{
        border-right: 2px solid var(color-borda);
        padding: 2px 12px 0 2px;
        font-size: var(--text-link);
    }
    button{
        margin-left: 6px;
        background-color: var(--color-laranja);
        font-size: var(--text-butao);
        cursor: pointer;
    }
    i{
        font-size: 33.5px;
        cursor: pointer;
        padding: 5px;
    }

    /* Menu resposivo */
    @media screen and (max-width: 1020px) {
        .cabecalho{
            flex-direction: column;
            padding: 10px 22px;
            height: fit-content;
        }
        .icone_menu{
            display: block;
        }
        .logo{
            padding: 7px 10px;
            width: 100%;
        }
        .navigation{
            display: none;
        }
        .menu{
            display: flex;
            flex-direction: column;
            padding: 10px 0;
            align-items: center;
            background: rgba(255, 255, 255, 0.001);
            backdrop-filter: blur(7px);
        }
        .links{
            flex-direction: column;
            align-items: left;
            padding-bottom: 10px;
            gap: 15px;
            padding: 0 10px;
        }
        .links a{
            font-size: var(--text-link-responsivo);
            border-bottom: 1px solid var(--color-branco);
            padding: 0 0px 5px 5px;
            border-right: none;
            width: var(--width-links);
        }
        button{
            font-size: var(--text-butao-responsivo);
            margin-top: 10px;
        }
        
    }
</style>