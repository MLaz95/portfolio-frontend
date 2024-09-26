<script>
  import Nav from './components/Nav.vue'
  import Hero from './components/Hero.vue'
  import About from './components/About.vue'
  import Skills from './components/Skills.vue'
  import Projects from './components/Projects.vue'

  export default{
    components:{
      Nav,
      Hero,
      About,
      Skills,
      Projects,
    }
  }

</script>

<template>
  <Nav></Nav>
  <Hero></Hero>
  <About></About>
  <Skills></Skills>
  <Projects></Projects>
</template>

<style scoped>

</style>
