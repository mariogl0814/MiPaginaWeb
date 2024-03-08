<script setup>
import { ref } from 'vue'

import html5 from '../assets/img/icono_html5.png'
import css from '../assets/img/icono_css.png'
import javascript from '../assets/img/icono_javascript.png'
import vue from '../assets/img/icono_vue.svg'
import github from '../assets/img/icono_github.png'

const destinos = ref([
    {
        nombre: 'HTML',
        rutaImagen: html5
    },
    {
        nombre: 'Javascript',
        rutaImagen: javascript
    },
    {
        nombre: 'CSS',
        rutaImagen: css
    },
    {
        nombre: 'Bootstrap',
        rutaImagen: css
    },
    {
        nombre: 'SASS',
        rutaImagen: css
    },
    {
        nombre: 'Tailwind',
        rutaImagen: css
    },
    {
        nombre: 'Vue',
        rutaImagen: vue
    },
    {
        nombre: 'Git',
        rutaImagen: github
    },

])
</script>

<template>
    <svg id="habilidades-id" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320">
        <path fill="#0099ff" fill-opacity="1"
            d="M0,0L34.3,37.3C68.6,75,137,149,206,165.3C274.3,181,343,139,411,106.7C480,75,549,53,617,53.3C685.7,53,754,75,823,106.7C891.4,139,960,181,1029,181.3C1097.1,181,1166,139,1234,138.7C1302.9,139,1371,181,1406,202.7L1440,224L1440,320L1405.7,320C1371.4,320,1303,320,1234,320C1165.7,320,1097,320,1029,320C960,320,891,320,823,320C754.3,320,686,320,617,320C548.6,320,480,320,411,320C342.9,320,274,320,206,320C137.1,320,69,320,34,320L0,320Z">
        </path>
    </svg>

    <section  class="habilidades">

        <div class="habilidades_contenedor contenedor seccion">
            <h2 class="habilidades__heading">Mis habilidades</h2>

            <ul class="habilidades__grid">
                <li v-for="(destino, index) in destinos" :key="index" class="habilidad">
                    <div class="habilidad__imagen">
                        <img :src="destino.rutaImagen" alt="imagen destino">
                    </div>

                    <div class="habilidad__informacion">
                        <h3 class="habilidad__nombre">{{ destino.nombre }}</h3>
                    </div>
                </li>
            </ul>
        </div>
    </section>

</template>

<style scoped></style>