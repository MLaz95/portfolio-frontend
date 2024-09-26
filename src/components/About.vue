<template>
    <section id="about">
        <p class="section__text">Get To Know More</p>
        <h1 class="title">About Me</h1>
        <div class="section-container">
            <div class="section__pic-container">
                <img src="/src/assets/Marco_crop.jpg" alt="Marco profile pic">
            </div>
            <div class="about-details-container">
                <p class="section-text-p3">
                    Hi! I’m Marco, a full-stack web developer based in Rome, Italy. Almost a year ago I decided to take the leap and pursue a career in tech, so I enrolled in a full-time immersive Web-Development course at Boolean.  Turns out coding is pretty fun! I love to learn new technologies and flex my problem solving skills to create interesting projects.
                </p>
                <p>
                    Beyond coding, I love games, travelling, cooking, and my cat!
                </p>
            </div>
        </div>
    </section>
</template>

<style>
    .section-container{
        display: flex;
        gap: 4rem;
        height: 80%;
        justify-content: center;
        align-items: center
    }

    .section__pic-container{
        width: 400px;
        height: 400px;
        flex-shrink: 0;
    }

    .section__pic-container img{
        width: 100%;
        height: 100%;
        border-radius: 50%;
    }

    .about-details-container{
        max-width: 45%;
    }

    .section-text-p3{
        margin-bottom: 1rem;
    }
</style>