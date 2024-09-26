<template>
    <ul class="links">
        <li><a @click="scrollFunction('about')">About</a></li>
        <li><a @click="scrollFunction('skills')">Skills</a></li>
        <li><a @click="scrollFunction('projects')">Projects</a></li>
        <li><a @click="scrollFunction('contact')">Contact</a></li>
    </ul>
</template>

<style>
    .links{
        list-style: none;
        display: flex;
        gap: 2rem;
        font-size: 1.5rem;
    }
</style>

<script>
    export default{
        methods:{
            scrollFunction(id){
                const element = document.getElementById(id)
                element.scrollIntoView({behavior: 'smooth'})
            }
        }
    }
</script>