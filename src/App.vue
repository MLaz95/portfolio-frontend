<script>
  import Nav from './components/Nav.vue'
  import Hero from './components/Hero.vue'
  import About from './components/About.vue'
  import Skills from './components/Skills.vue'
  import Projects from './components/Projects.vue'
  import Contact from './components/Contact.vue'
  import Footer from './components/Footer.vue'

  export default{
    components:{
      Nav,
      Hero,
      About,
      Skills,
      Projects,
      Contact,
      Footer,
    }
  }

</script>

<template>
  <Nav></Nav>
  <Hero></Hero>
  <About></About>
  <Skills></Skills>
  <Projects></Projects>
  <Contact></Contact>
  <Footer></Footer>
</template>

<style scoped>

</style>
