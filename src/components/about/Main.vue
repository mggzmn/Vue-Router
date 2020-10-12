<template>
<section class="main">
    <article class="about">
        <div class="container">
            <div class="picture">
                <img src="../../assets/picture.jpg" alt="mggzmn Mariana" />
            </div>
            <div class="text">
                <Title text="Sobre mí" />
                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum</p>
            </div>
        </div>
    </article>
    <article class="works">
        <div class="container">
            <Title text="Trabajos" />
            <div class="container-works">
                <Work v-for="(item) in works" v-bind:key="item.id" v-bind:description="item.description" :title="item.title" />
            </div>
        </div>
    </article>
</section>
</template>

<script>
import Title from '@/components/Title.vue'
import Work from '@/components/about/Work.vue'

export default {

    name: 'Main',
    components: {
        Title,
        Work
    },
    data() {
        return {
            works: [{
                    id: 1,
                    image: '../../assets/logo.png',
                    title: 'Ut enim ad minim',
                    description: 'HTML - CSS - VUE'
                },
                {
                    id: 2,
                    image: '../../assets/logo.png',
                    title: 'Ut enim ad minim',
                    description: 'HTML - CSS - VUE'
                },
                {
                    id: 3,
                    image: '../../assets/logo.png',
                    title: 'Ut enim ad minim',
                    description: 'HTML - CSS - VUE'
                }
            ]
        }
    }
}
</script>

<style>
.picture img {
    height: 115px;
}
</style>
