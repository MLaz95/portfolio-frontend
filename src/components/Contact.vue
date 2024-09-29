<template>
    <section id="contact">
        <p class="section__text">
            Get in Touch
        </p>
        <h1 class="title">Contact Me</h1>
        <div class="contact-container">

            <a href="mailto:lazzari.marco.ml@gmail.com" target="_blank">
                <div class="contact-info">
                    <img class="icon" src="/src/assets/email.png" alt="email icon">
                    <div>lazzari.marco.ml@gmail.com</div>
                </div>
            </a>

            <a href="https://www.linkedin.com/in/marco-lazzari-6767502b9" target="_blank">
                <div class="contact-info">
                    <img class="icon" src="/src/assets/linkedin.png" alt="linkedin icon">
                    <div>LinkedIn</div>
                </div>
            </a>

        </div>
    </section>
</template>

<style>
#contact {
    display: flex;
    flex-direction: column;
    justify-content: center;
    height: 96vh;
}

.contact-container {
    display: flex;
    justify-content: center;

    border: 1px solid gray;
    border-radius: 2rem;
    margin: 2rem auto;
    padding: 0.5rem;
}

.contact-info {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 0.5rem;
    margin: 1rem;
    font-size: larger;
}

a:hover .icon {
    filter: drop-shadow(1px 2px var(--highlight));
}
</style>