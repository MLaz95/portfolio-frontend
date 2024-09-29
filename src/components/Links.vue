<template>
    <ul class="links">
        <li><a @click="scrollFunction('about')">About</a></li>
        <li><a @click="scrollFunction('skills')">Skills</a></li>
        <li><a @click="scrollFunction('projects')">Projects</a></li>
        <li><a @click="scrollFunction('contact')">Contact</a></li>
    </ul>
    
    <div id="mobile-menu" ref="dropDown">
        <i @click="openMenu()" id="menu-btn" class="fa-solid fa-bars"></i>

        <Transition name="open" appear>
            <ul class="mobile-links" v-show="isMenuActive">
                <li><a @click="scrollFunction('about')">About</a></li>
                <li><a @click="scrollFunction('skills')">Skills</a></li>
                <li><a @click="scrollFunction('projects')">Projects</a></li>
                <li><a @click="scrollFunction('contact')">Contact</a></li>
            </ul>
        </Transition>
    </div>
</template>

<style>
.links {
    list-style: none;
    display: flex;
    gap: 2rem;
    font-size: 1.5rem;
}

#mobile-menu {
    display: none;
}

#menu-btn {
    font-size: 1.5rem;
}

.mobile-links {
    position: fixed;
    top: 1px;
    right: 1px;
    z-index: 1;

    width: 50%;
    border: 1px solid gray;
    border-radius: 1rem;
    background-color: white;

    list-style: none;
    font-size: 1.5rem;
    padding: 1rem;
}

.mobile-links li {
    padding: 0.5rem;
}

.open-enter-active,
.open-leave-active {
  transition: all 0.3s ease-out;
}

.open-enter-from,
.open-leave-to {
  transform: translateX(20px);
  opacity: 0;
}

</style>

<script>
export default {
    data(){
        return{
            isMenuActive: false,
        }
    },

    mounted(){
        window.addEventListener('click', this.closeMenu)
    },

    beforeUnmount(){
        window.removeEventListener('click', this.closeMenu)
    },

    methods: {
        scrollFunction(id) {
            const element = document.getElementById(id)
            element.scrollIntoView({ behavior: 'smooth' })
            this.isMenuActive = false
        },

        openMenu(){
            this.isMenuActive = true;
        },

        closeMenu(element){
            if(!this.$refs.dropDown.contains(element.target)){
                this.isMenuActive = false;
            }
        }
    }
}
</script>