<template>
    <div class="proyectos--container">
        <span>
            <h2>Portafolio de proyectos</h2>
            <hr class="title--separator">
        </span>
        <div class="proyectos">
            <Proyecto class="proyecto--component" v-for="proyecto in proyectos" :key="proyecto.id" :image="proyecto.image" :title="proyecto.title" :description="proyecto.description"></Proyecto>
        </div>
    </div>
</template>

<script>
import Proyecto from '../components/Proyecto.vue';

export default {
    components: {
        Proyecto
    },
    data: function() {
        return  {
            proyectos: [
                {
                    id: '1',
                    title: 'Proyecto 1',
                    description: 'Proyecto 1',
                    image: 'https://www.w3schools.com/w3css/img_lights.jpg'
                },
                {
                    id: '2',
                    title: 'Proyecto 2',
                    description: 'Proyecto 2',
                    image: 'https://images.pexels.com/photos/414612/pexels-photo-414612.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500'
                },
                {
                    id: '3',
                    title: 'Proyecto 3',
                    description: 'Proyecto 3',
                    image: 'https://images.pexels.com/photos/462118/pexels-photo-462118.jpeg?auto=format%2Ccompress&cs=tinysrgb&dpr=1&w=500'
                },
                {
                    id: '4',
                    title: 'Proyecto 4',
                    description: 'Proyecto 4',
                    image: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTsgKWaWvMfgSmQjJBETlectexGQ4qM_Yf4eiP44iWKUqBASfGvUA'
                },
                {
                    id: '5',
                    title: 'Proyecto 5',
                    description: 'Proyecto 5',
                    image: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTsgKWaWvMfgSmQjJBETlectexGQ4qM_Yf4eiP44iWKUqBASfGvUA'
                }
            ]
        }
    }
}
</script>


<style lang="scss" scoped>
    @import '../assets/variables';
    .proyectos--container {
        padding: 15px 30px 30px 30px;
        min-height: 91vh;
        width: 100%;
        background-color: $principal;
    }
    .title--separator {
        height: 4px;
        width: 100px;
        background-color: $black;
        border-style: none;
        margin-top: 15px;
        margin-bottom: 15px;
        animation-name: divisorAnimacion;
        animation-duration: 4s;
    }
    @keyframes divisorAnimacion {
        0%  {
            width: 0%
        }
        100% {
            width: 100px
        }
    }

    .proyectos {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        @media only screen and(max-width: 800px) {
            grid-template-columns: repeat(2, 1fr);
        }
        @media only screen and(max-width: 640px) {
            grid-template-columns: repeat(1, 1fr);
        }
        .proyecto--component:nth-child(5) {
            grid-column: 2 / 4;
            @media only screen and(max-width: 800px) {
                grid-column: 1 / 3;
            }
            @media only screen and(max-width: 640px) {
                grid-column: 1;
            }
        }
    }
</style>
