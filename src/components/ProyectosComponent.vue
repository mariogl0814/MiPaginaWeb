<script setup>
    import {ref} from 'vue'
    import proyecto1 from '../assets/img/proyecto_01.png'
    import proyecto2 from '../assets/img/proyecto_02.png'
    import proyecto3 from '../assets/img/proyecto_03.png'
    import proyecto4 from '../assets/img/proyecto_04.png'
    import proyecto5 from '../assets/img/proyecto_05.png'
    import proyecto6 from '../assets/img/proyecto_06.png'
    import proyecto7 from '../assets/img/proyecto_07.png'
    import proyecto8 from '../assets/img/proyecto_08.png'

    const proyectos = ref([
        {
            rutaImagen: proyecto1,
            nombre: '01 Ecommerce',
            rutaPagina: 'https://ecommerceview.netlify.app'
        },
        {
            rutaImagen: proyecto2,
            nombre: '02 TechPro',
            rutaPagina: 'https://02audifonos.netlify.app'
        },
        {
            rutaImagen: proyecto3,
            nombre: '03 Casas',
            rutaPagina: 'https://03arquitecturavue.netlify.app'
        },        
        {
            rutaImagen: proyecto4,
            nombre: '04 Nucleus',
            rutaPagina: 'https://04nucleus.netlify.app'
        },       
        {
            rutaImagen: proyecto5,
            nombre: '05 Delivery',
            rutaPagina: 'https://05delivery.netlify.app'
        },        
        {
            rutaImagen: proyecto6,
            nombre: '06 Podcast',
            rutaPagina: 'https://06podcast.netlify.app'
        },        
        {
            rutaImagen: proyecto7,
            nombre: '07 Viajes',
            rutaPagina: 'https://07viajes.netlify.app'
        },        
        {
            rutaImagen: proyecto8,
            nombre: '08 Agencia de viajes',
            rutaPagina: 'https://08realstate.netlify.app/'
        }
    ])
</script>

<template>
    <section id="proyectos-id" class="proyectos contenedor seccion">
        <h2 class="proyectos__heading">Proyectos realizados en Vue</h2>

        <div class="proyectos__grid">
            <div v-for="(proyecto, index) in proyectos" :key="index" class="proyecto">
                <a :href="proyecto.rutaPagina">
                    <div class="proyecto__icontenedor">
                        <img class="proyecto__icontenedor--imagen" :src="proyecto.rutaImagen" alt="imagen seccion proyecto">
                    </div>
                    <p class="proyecto__nombre">{{ proyecto.nombre }}</p>
                </a>
            </div>
        </div>

    </section>

</template>

<style scoped></style>