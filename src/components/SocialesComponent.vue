<script setup>
    import { ref } from 'vue'
    import facebook from '../assets/img/icono_facebook.svg'
    import instagram from '../assets/img/icono_instagram.svg'
    import linkedin from '../assets/img/icono_linkedin.png'
    import github from '../assets/img/icono_github.png'

    const sociales = ref([
        {
            rutaImagen: facebook ,
            rutaSocial: 'https://www.facebook.com/mario.garlo/'
        },
        {
            rutaImagen: instagram ,
            rutaSocial: 'https://www.instagram.com/garlomario/'
        },
        {
            rutaImagen: linkedin ,
            rutaSocial: 'https://www.linkedin.com/in/mario-garc%C3%ADa-l%C3%B3pez-38851524a/'
        },
        {
            rutaImagen: github ,
            rutaSocial: 'https://github.com/mariogl0814'
        },
    ])


</script>
  
<template>
    <section id="sociales-id" class="sociales">
        <div class="contenedor seccion">
            <h2 class="sociales__heading">Mis redes sociales</h2>

            <ul class="sociales__lista">
                <li v-for="(social,index) in sociales" :key="index" class="sociales__elemento">
                    <a :href="social.rutaSocial">
                        <img :src="social.rutaImagen" alt="social">
                    </a>
                </li>
            </ul>
        </div>
    </section>

</template>
  
<style scoped>
  
</style>
  