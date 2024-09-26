<template>
    <nav>
        <div id="logo">Marco Lazzari</div>
        <Links></Links>
    </nav>
</template>

<style>
nav {
    display: flex;
    justify-content: space-around;
    align-items: center;
    height: 15vh;
}

#logo {
    font-size: 2rem;
}
</style>

<script>
import Links from './Links.vue'

export default {
    components: {
        Links,
    }
}
</script>