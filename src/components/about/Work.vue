<template>
<div class="work">
    <div class="thumb">
        <img src="../../assets/logo.png" :alt="title" />
    </div>
    <div class="description">
        <p class="name">{{title}}</p>
        <p class="category">{{description}}</p>
    </div>
</div>
</template>

<script>
export default {
    name: 'Work',
    props: ['title', 'image', 'description']
}
</script>

<style>
@media screen and (max-width:800px) {
    .work {
        width: 40%
    }
}
</style>
