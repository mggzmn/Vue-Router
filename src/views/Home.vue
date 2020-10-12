<template>
<div>
    <!--<img alt="Vue logo" src="../assets/logo.png">-->
    <Header name="Welcome to Mariana's App" role="Vue Router" />
    <div class="container">
        <div class="text">
            <Title text="Vue.js App" />
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum</p>
        </div>
    </div>
</div>
</template>

<script>
// @ is an alias to /src
//import HelloWorld from '@/components/HelloWorld.vue'
import Title from '@/components/Title.vue'
import Header from '@/components/Header.vue'
export default {
    name: 'Home',
    components: {
        Title,
        Header
    }
}
</script>
