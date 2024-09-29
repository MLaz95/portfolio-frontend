<template>
    <nav>
        <div id="logo"><a @click="scrollTop()">Marco Lazzari</a></div>
        <Links></Links>
    </nav>
</template>

<style>
nav {
    position: fixed;
    z-index: 1;
    top: 0;
    left: 0;
    width: 100%;
    background-color: white;

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
    },

    methods:{
        scrollTop(){
            window.scrollTo({
                top: 0,
                behavior: 'smooth'
            })
        }
    }
}
</script>