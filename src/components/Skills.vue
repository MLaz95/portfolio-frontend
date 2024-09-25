<template>
    <section>
        <p class="section__text">Explore My</p>
        <h1 class="title">Skills</h1>

        <div class="skills-container">
            <div class="skill-box">
                <h2 class="skill-sub-title">Frontend</h2>
                <div class="skills-wrapper">
                    <div class="skill-item">
                        <i class="fa-brands fa-html5"></i>
                        <div>HTML5</div>
                    </div>
                    <div class="skill-item">
                        <i class="fa-brands fa-html5"></i>
                        <div>HTML5</div>
                    </div>
                    <div class="skill-item">
                        <i class="fa-brands fa-html5"></i>
                        <div>HTML5</div>
                    </div>
                    <div class="skill-item">
                        <i class="fa-brands fa-html5"></i>
                        <div>HTML5</div>
                    </div>
                </div>
            </div>
            <div class="skill-box">
                <h2 class="skill-sub-title">Backend</h2>
                <div class="skills-wrapper">
                    
                </div>
            </div>
        </div>
    </section>
</template>

<style>
    .skills-container{
        display: flex;
        gap: 2rem;
    }

    .skill-box{
        /* background-color: pink; */
        /* height: 100px; */
        /* test */
        flex: 1;
        border-radius: 2rem;
        border: 1px solid gray;

        text-align: center;
        padding: 1.5rem;
    }

    .skill-sub-title{
        color: rgb(85, 85, 85);
        font-weight: 600;
        font-size: 1.75rem;
        margin-bottom: 2rem;
    }

    .skills-wrapper{
        display: flex;
        justify-content: start;
        flex-wrap: wrap;
        row-gap: 2rem;
    }

    .skills-wrapper .fa-brands{
        font-size: 4rem;
    }

    .skill-item{
        width: calc(100% / 3);
    }
</style>