<template>
<div>
    <Header name="Mariana Guzmán" role="Ingeniera en Sistemas" />
    <Main />
</div>
</template>

<script>
//import Title from '@/components/Title.vue'
import Header from '@/components/Header.vue'
import Main from '@/components/about/Main.vue'

export default {
    name: 'About',
    components: {
        Header,
        Main
    }
}
</script>

<style>
.main .container {
    overflow: visible;
}

.about {
    text-align: center;
}

.picture {
    margin-top: -60px;
}

.picture img {
    vertical-align: top;
    border-radius: 50%;
    border: 5px solid rgba(255, 255, 255, .2)
}

.works {
    background: #f2f2f2;
    padding: 60px 0;
}

.works .container {
    overflow: hidden;
}

.works .container h1 {
    color: #2c3e50 !important;
}

.container-works {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: space-between;
}

.main .works .container-work .work {
    width: 23%;
}

.main .works .container-work .work .thumb {
    width: 100%;
    margin-bottom: 10px;
}

.main .works .container-work .work .thumb img {
    width: 100%;
    vertical-align: top;
    border-radius: 3px;
}

.description {
    text-align: left;

}

.description .name {
    font-weight: bold;
    color: #42b983;
    margin-bottom: 10px;
    text-shadow: none;
    font-size: .8rem;
}

.description .category {
    color: #2c3e50;
    font-size: .6rem;
}
</style>
