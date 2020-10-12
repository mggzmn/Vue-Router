<template>
<Header name="Post" :role="`${$route.params.id}`" />

<div class="container">
    <div class="text">
        <Title :text="article.title" />
        <p>{{article.body}}</p>
    </div>
</div>
</template>

<script>
import Header from "../components/Header";
import Title from "../components/Title";
export default {
    name: 'Article',
    components: {
        Title,
        Header
    },
    data() {
        return {
            article: {}
        }
    },
    methods: {
        async getArticles() {
            try {
                const data = await fetch(`https://jsonplaceholder.typicode.com/posts/${this.$route.params.id}`)
                const obj = await data.json();
                this.article = obj;
            } catch (error) {
                console.log(error)
            }
        }
    },
    created() {
        this.getArticles()
    }
}
</script>

<style>

</style>
