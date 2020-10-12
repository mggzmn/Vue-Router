<template>
<div class="text-container">
    <div class="text">
        <h1 class="name">{{name}}</h1>
        <h2 class="role"> {{role}}</h2>
    </div>
</div>
</template>

<script>
export default {
    name: 'BoxText',
    props: ['name', 'role'],
}
</script>

<style>
header .text-container {
    display: flex;
    justify-content: center;
    align-content: center;
    margin: 100px 0;
}

header .text-container .text {
    border: 2px solid rgba(255, 255, 255, 0.5);
    border-radius: 3px;
    display: inline-block;
    text-align: center;
    padding: 1rem 1.5rem;
}

.name,
.role {
    color: #fff;
    font-weight: bold;
    margin: 0;
    text-shadow: 1px 1px 2px black;
}

.name {
    margin-bottom: 10px;
    font-size: 1.5rem;
    line-height: 1.5rem;
}

.role {
    font-size: .8rem;
    line-height: .5rem;
}
</style>
