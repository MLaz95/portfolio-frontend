<template>
    <section>
        <p class="section__text">Explore My</p>
        <h1 class="title">Skills</h1>

        <div class="skills-container">

            <div class="skill-box">
                <h2 class="skill-sub-title">Frontend</h2>
                <div class="skills-wrapper">
                    <div v-for="skill in frontend" class="skill-item">
                        <i :class="skill.icon" :style="'color:' + skill.color"></i>
                        <div>{{ skill.name }}</div>
                    </div>
                </div>
            </div>

            <div class="skill-box">
                <h2 class="skill-sub-title">Backend</h2>
                <div class="skills-wrapper">
                    <div v-for="skill in backend" class="skill-item">
                        <i :class="skill.icon" :style="'color:' + skill.color"></i>
                        <div>{{ skill.name }}</div>
                    </div>
                </div>
            </div>

            <div class="skill-box">
                <h2 class="skill-sub-title">Miscellaneous</h2>
                <div class="skills-wrapper">
                    <div v-for="skill in misc" class="skill-item">
                        <i :class="skill.icon" :style="'color:' + skill.color"></i>
                        <div>{{ skill.name }}</div>
                    </div>
                </div>
            </div>
        </div>

    </section>
</template>

<style>
.skills-container {
    display: flex;
    gap: 2rem;
    margin-top: 3rem;
    padding: 0 5rem;
    flex-wrap: wrap;
}

.skill-box {
    flex: 1 0 45%;
    border-radius: 2rem;
    border: 1px solid gray;

    text-align: center;
    padding: 1.5rem;
}

.skill-sub-title {
    color: rgb(85, 85, 85);
    font-weight: 600;
    font-size: 1.75rem;
    margin-bottom: 2rem;
}

.skills-wrapper {
    display: flex;
    justify-content: start;
    flex-wrap: wrap;
    row-gap: 2rem;
}

.skills-wrapper i {
    font-size: 4rem;
}

.skill-item {
    width: calc(100% / 3);
}
</style>

<script>
export default {
    data() {
        return {
            frontend: [
                {
                    name: 'HTML5',
                    icon: 'fa-brands fa-html5',
                    color: '#e34f26',
                },
                {
                    name: 'CSS',
                    icon: 'fa-brands fa-css3-alt',
                    color: '#264de4',
                },
                {
                    name: 'JavaScript',
                    icon: 'fa-brands fa-js',
                    color: '#f0db4f',
                },
                {
                    name: 'Sass',
                    icon: 'fa-brands fa-sass',
                    color: '#cd6d93',
                },
                {
                    name: 'Bootstrap',
                    icon: 'fa-brands fa-bootstrap',
                    color: '#563d7c',
                },
                {
                    name: 'Vue',
                    icon: 'fa-brands fa-vuejs',
                    color: '#42b883',
                },

            ],

            backend: [
                {
                    name: 'PHP',
                    icon: 'fa-brands fa-php',
                    color: '#474A8A',
                },
                {
                    name: 'Laravel',
                    icon: 'fa-brands fa-laravel',
                    color: '#f05340',
                },
                {
                    name: 'MySql',
                    icon: 'fa-solid fa-database',
                    color: 'gray',
                },
            ],

            misc: [
                {
                    name: 'Git',
                    icon: 'fa-brands fa-git-alt',
                    color: '#f1502f',
                },
                {
                    name: 'RESTful API',
                    icon: 'fa-solid fa-gears',
                    color: '',
                },
                {
                    name: 'npm',
                    icon: 'fa-brands fa-npm',
                    color: '#CC3534',
                },
            ]
        }
    }
}
</script>