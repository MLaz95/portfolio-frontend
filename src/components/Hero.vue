<template>
    <section id="profile">
        <div id="hero-top-box">
            <p class="hero-text">Hello! My name is</p>

            <svg id="hero-svg" viewBox="0 0 168 52" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path id="hero-name"
                    d="M44.536 24.8079C44.3404 23.2431 41.3581 23.3086 40.3328 23.2395C35.3661 22.9047 29.9849 24.7846 25.4021 26.439C18.8117 28.8181 11.6273 31.9439 6.33085 36.6647C4.10584 38.6478 0.83349 43.0115 3.44508 46.0121C5.8697 48.7978 11.7596 46.7481 14.3608 45.4474C20.4882 42.3838 25.0978 36.5134 28.727 30.8931C32.7049 24.7328 36.7386 17.6008 38.3881 10.379C38.8851 8.20277 37.9255 -1.72661 34.9377 4.1683C32.6418 8.69792 31.2226 13.5731 30.5463 18.5972C29.9993 22.6608 28.6625 29.3926 30.9227 33.2143C36.7107 43.0012 49.9344 16.8098 51.0604 13.3275C51.7464 11.2058 53.2473 7.18896 52.3151 4.85838C51.9284 3.89182 49.4183 11.0251 49.3666 11.1945C46.7913 19.6225 43.8328 28.0467 42.2149 36.7274C41.6658 39.6731 39.5157 47.9932 43.7832 49.5252C49.0658 51.4215 55.4628 45.2936 55.8282 40.1778C55.9066 39.0805 55.8234 40.7846 55.8282 40.9933C55.8707 42.8643 56.1027 44.9127 58.463 44.8828C64.8139 44.8024 71.6994 35.9405 69.567 29.7011C68.5223 26.6443 64.709 27.8913 62.7917 29.1365C58.9771 31.6141 56.6913 35.4377 56.0791 39.9268C54.79 49.3807 62.8298 49.13 67.434 42.7499C68.5732 41.1713 70.4 37.5038 68.6887 35.6609C67.2288 34.0887 65.8944 36.879 65.552 37.9193C64.9008 39.8979 64.0725 43.9621 65.9284 45.5729C68.9002 48.1522 74.477 46.0672 77.0637 43.9732C80.7366 40.9999 83.4126 32.7184 78.4753 29.7011C77.8721 29.3326 76.9112 29.2899 77.597 30.1717C78.5812 31.4371 80.463 31.5476 81.9256 31.4891C85.1548 31.3599 88.0812 30.1164 91.1162 29.1679C92.9433 28.597 87.817 31.1247 86.2857 32.2733C83.413 34.4278 75.3173 46.7021 83.9018 46.7021C91.3778 46.7021 97.9261 40.9252 102.346 35.5354C102.832 34.9428 109.081 25.4828 105.765 27.6937C101.43 30.5836 97.1073 37.5692 97.1073 42.8126C97.1073 50.0279 108.704 48.7107 112.665 46.4826C113.088 46.2449 118.938 40.115 115.959 40.115C115.053 40.115 116.222 44.0905 118.562 43.9105C124.636 43.4433 131.357 35.7324 130.796 29.7011C130.182 23.1001 114.797 30.8525 116.116 37.4488C117.707 45.406 126.841 40.0965 129.51 36.2569C131.178 33.8565 138.154 22.2583 131.454 20.9184C127.721 20.1717 118.891 27.5864 124.177 30.2971C128.658 32.5948 135.583 29.472 139.735 27.8505C148.61 24.385 157.184 20.1196 165.927 16.3388"
                    stroke="#c1121f" stroke-width="3" stroke-linecap="round" />
            </svg>

            <p class="hero-text">I'm a Full-Stack Developer.</p>
        </div>

        <div class="hero-links">
            <div class="btn-container">
                <a href="/Marco.Lazzari.CV.pdf" download>
                    <button class="btn btn-color-1">
                        Download CV
                    </button>
                </a>
                <a @click="scrollFunction('contact')">
                    <button class="btn btn-color-1">
                        Contact Me
                    </button>
                </a>
            </div>

            <div id="socials-container">
                <a href="https://github.com/MLaz95" target="_blank">
                    <img class="icon" src="/src/assets/github.png" alt="github">
                </a>
                <a href="https://www.linkedin.com/in/marco-lazzari-6767502b9" target="_blank">
                    <img class="icon" src="/src/assets/linkedin.png" alt="linkedin">
                </a>
            </div>
        </div>
    </section>
</template>

<style>
#profile {
    height: 85vh;
    margin-top: 15vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 3rem;
}

#hero-top-box {
    display: flex;
    flex-direction: column;
    /* justify-content: center; */
    gap: 0.5rem;
}

#hero-svg {
    width: 700px;
}

#hero-name {
    stroke-dasharray: 633.67919921875;
    stroke-dashoffset: 633.67919921875;
    animation: sign 4s ease;
    animation-fill-mode: forwards;
}

@keyframes sign {
    to {
        stroke-dashoffset: 0;
    }
}

.hero-text {
    font-size: 3rem;
}

.btn-container {
    display: flex;
    justify-content: center;
    gap: 1rem;
}

#socials-container {
    display: flex;
    justify-content: center;
    gap: 1rem;
    margin-top: 1rem;
}

.icon {
    height: 2rem;
}

#profile .icon:hover{
    filter: drop-shadow(1px 2px var(--highlight));
}
</style>

<script>
export default{
    methods:{
        scrollFunction(id) {
            const element = document.getElementById(id)
            element.scrollIntoView({ behavior: 'smooth' })
            this.isMenuActive = false
        },
    }
}
</script>