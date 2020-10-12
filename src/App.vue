<template>
<div>
    <div id="nav">
        <router-link to="/">Home</router-link> |
        <router-link to="/about">About</router-link> |
        <router-link to="/blog">Blog</router-link>
    </div>
    <router-view />
</div>
</template>

<style>
* {
    box-sizing: border-box;
}

#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    font-size: 1rem;
}

#nav {
    padding: 30px;
}

#nav a {
    font-weight: bold;
    color: #2c3e50;
}

#nav a.router-link-exact-active {
    color: #42b983;
}

.container {
    width: 90%;
    max-width: 1000px;
    margin: auto;
    overflow: hidden;
}

.text {
    color: #5a5a5a;
    font-weight: bold;
    font-size: 1rem;
    line-height: 2rem;
    width: 80%;
    margin: 40px auto 60px auto;
    text-align: justify;

}
</style>
