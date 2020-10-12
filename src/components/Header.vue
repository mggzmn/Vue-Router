<template>
<header>
    <div class="container">
        <BoxText :name="name" :role="role" />
    </div>
</header>
</template>

<script>
import BoxText from './BoxText';

export default {
    name: 'Header',
    props: ['name', 'role'],
    components: {
        BoxText
    }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Montserrat&display=swap');

header {
    background: url('../../public/img/header.jpg');
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover;
    max-height: 600px;
    font-family: 'Montserrat', sans-serif;

}
</style>
