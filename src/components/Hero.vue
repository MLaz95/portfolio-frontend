<template>
    <section id="profile">
        <div class="section__pic-container">
            <img src="/src/assets/Marco_crop.jpg" alt="Marco Lazzari profile picture">
        </div>
        <div class="section__text">
            <p class="section__text__p1">Hello, I'm</p>
            <h1 class="title">Marco Lazzari</h1>
            <p class="section__text__p2">Full-Stack Developer</p>
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
        /* background-color: pink; */
        /* test */
        height: 85vh;
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 5rem;
    }

    #profile *{
        /* border: 1px dashed red; */
        /* test */
    }

    .section__pic-container{
        width: 400px;
        height: 400px;
    }

    .section__pic-container img{
        width: 100%;
        height: 100%;
        border-radius: 50%;
    }

    .section__text{
        text-align: center;
    }

    .section__text p{
        font-weight: 600;
        color: gray;
    }

    .section__text__p2{
        font-size: 1.75rem;
        margin-bottom: 1rem;
    }

    .title{
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