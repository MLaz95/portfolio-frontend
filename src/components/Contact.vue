<template>
    <section id="contact">
        <p class="section__text">
            Get in Touch
        </p>
        <h1 class="title">Contact Me</h1>
        <div class="contact-container">
            <div class="contact-info">
                <img class="icon" src="/src/assets/email.png" alt="email icon">
                <a href="mailto:lazzari.marco.ml@gmail.com" target="_blank">Example@gmail.com</a>
            </div>
            <div class="contact-info">
                <img class="icon" src="/src/assets/linkedin.png" alt="linkedin icon">
                <a href="https://www.linkedin.com/in/marco-lazzari-6767502b9"  target="_blank">LinkedIn</a>
            </div>
        </div>
    </section>
</template>

<style>
    #contact{
        display: flex;
        flex-direction: column;
        justify-content: center;
        height: 96vh;
    }

    .contact-container{
        display: flex;
        justify-content: center;
        /* gap: 2rem; */

        border: 1px solid gray;
        border-radius: 2rem;
        margin: 2rem auto;
        padding: 0.5rem;
    }

    .contact-info{
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 0.5rem;
        margin: 1rem;
    }

    .contact-info i{
        font-size: 2rem;
    }

    .contact-info a{
        font-size: larger;
    }
</style>