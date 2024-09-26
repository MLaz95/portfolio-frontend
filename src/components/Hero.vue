<template>
    <section id="profile">
        <!-- <div class="section__pic-container">
            <img src="/src/assets/Marco_crop.jpg" alt="Marco Lazzari profile picture">
        </div> -->
        <div>
            <p class="hero-text">Hello! My name is</p>
            <h1 class="hero-title">Marco Lazzari</h1>
            <p class="hero-text">I'm a Full-Stack Developer.</p>
        </div>

        <div class="hero-links">
            <div class="btn-container">
                <button class="btn btn-color-1">
                    Download CV
                </button>
                <button class="btn btn-color-2">
                    Contact Me
                </button>
            </div>

            <div id="socials-container">
                <img class="icon" src="/src/assets/github.png" alt="github">
                <img class="icon" src="/src/assets/linkedin.png" alt="linkedin">
            </div>
        </div>
    </section>
</template>

<style>
    #profile{
        height: 85vh;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        gap: 3rem;
    }

    .hero-title{
        font-size: 6rem;
    }

    .hero-text{
        font-size: 3rem;
    }

    .btn-container{
        display: flex;
        justify-content: center;
        gap: 1rem;
    }

    #socials-container{
        display: flex;
        justify-content: center;
        gap: 1rem;
        margin-top: 1rem;
    }

    .icon{
        height: 2rem;
    }
</style>