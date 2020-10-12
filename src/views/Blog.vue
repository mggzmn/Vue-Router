<template>
<div>
    <!--<img alt="Vue logo" src="../assets/logo.png">-->
    <Header name="Welcome to Mariana's Blog" role="Blog" />
    <div class="container">
        <div class="text">
            <Title text="Mi Blog" />
        </div>
        <div class="articles">
            <div class="article" v-for="item in arrBlog" :key="item.id">
                <div class="article-title">{{item.title}}</div>
                <div class="article-body">{{item.body.substr(0,15)}}...</div>
                <router-link :to="`/blog/${item.id}`" tag="button" class="button">
                    Más</router-link>
            </div>
        </div>
    </div>
</div>
</template>

<script>
import Title from '../components/Title.vue'
import Header from '../components/Header.vue'
export default {
    name: 'Blog',
    components: {
        Title,
        Header
    },
    data() {
        return {
            arrBlog: [],
        }
    },
    created() {
        this.consumirApi()
    },
    methods: {
        async consumirApi() {
            try {
                const data = await fetch('https://jsonplaceholder.typicode.com/posts');
                const array = await data.json();
                this.arrBlog = array;
            } catch (error) {
                console.log(error);
            }
        }
    }
}
</script>

<style>
.button {
    display: inline-block;
    text-decoration: none;
    width: 80%;
    padding: .5rem;
    border: 1px solid #2c3e50;
    background: transparent;
    color: #2c3e50;
    box-shadow: 2px 5px 3px 0px rgba(0, 0, 0, 0.5);
}

.button:hover {
    border: 1px solid #42b983;
}

.articles {
    display: flex;
    flex-direction: column;
}

.article {
    padding: 1rem;
    width: 80%;
    margin: 1.5rem auto;
    border-radius: 3px;
    box-shadow: -1px 13px 26px -8px rgba(0, 0, 0, 0.75);
}

.article-title {
    color: #42b983;
    margin: 1rem;
}

.article-body {

    margin-bottom: 1.5rem;
}
</style>
