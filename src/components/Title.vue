<template>
<h1>{{text}}</h1>
</template>

<script>
export default {
    props: {
        text: String
    }

}
</script>

<style scoped>
h1 {
    font-size: 1.5rem;
    margin-bottom: 1.5rem;
    font-weight: bold;
    color: #42b983;
    text-align: center;
}
</style>
