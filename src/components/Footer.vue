<template>
    <footer>
        <!-- <Links></Links> -->
        <p>Copyright &copy; 2024 Marco Lazzari. All rights reserved.</p>
    </footer>
</template>

<style>
    footer{
        height: 4vh;
        display: flex;
        flex-direction: column;
        justify-content: space-around;
        align-items: center;
    }

    footer p{
        color: gray;
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