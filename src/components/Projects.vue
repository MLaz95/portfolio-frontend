<template>
    <section id="projects">
        <p class="section__text">Browse Some of My</p>
        <h1 class="title">Projects</h1>

        <div class="projects-container">
            <div v-for="proj in projects" class="project-card">
                <img class="project-cover" :src="proj.cover" alt="">
                <div class="project-info">
                    <h2>{{ proj.title }}</h2>
                    <div class="tech-container">
                        <div v-for="tech in proj.tech" class="tech">{{ tech }}</div>
                    </div>
                    <p>
                        {{ proj.description }}
                    </p>
                    <div class="btn-container">
                        <button class="btn btn-color-1">Github</button>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<style>

    .projects-container{
        display: flex;
        gap: 2rem;

        margin-top: 3rem;
    }

    .project-card{
        /* height: 700px; */
        /* test */
        flex: 1;
        border: 1px solid gray;
        border-radius: 2rem;
        padding: 1.5rem;

        display: flex;
        flex-direction: column;
        justify-content: space-between
    }

    .project-cover{
        width: 100%;
        border-radius: 2rem;
    }

    .project-info{
        flex: 1;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        padding: 2rem;
    }

    .project-info h2{
        font-size: 1.75rem;
    }

    .tech-container{
        display: flex;
        gap: 0.5rem;
        /* margin: 1rem 0; */
    }

    .tech{
        padding: 0 0.5rem;
        border: 1px solid gray;
        border-radius: 0.5rem;
    }



    .project-info h2{
        text-align: center
    }

</style>

<script>

    export default{
        data(){
            return{
                projects:[
                    {
                        cover:'https://upload.wikimedia.org/wikipedia/commons/thumb/1/15/Cat_August_2010-4.jpg/1200px-Cat_August_2010-4.jpg',
                        title:'Cat Proj',                        
                        description:'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Aperiam necessitatibus rerum molestiae cum itaque sint natus, mollitia nostrum ratione dolores. Ea nihil at a doloremque enim facilis natus sed et?',
                        link:'',
                        tech:[
                            'test',
                            'test',
                            'test',
                        ],
                    },
                    {
                        cover:'https://upload.wikimedia.org/wikipedia/commons/thumb/1/15/Cat_August_2010-4.jpg/1200px-Cat_August_2010-4.jpg',
                        title:'Cat Proj',                        
                        description:'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Aperiam necessitatibus rerum molestiae cum itaque sint natus, mollitia nostrum ratione dolores. Ea nihil at a doloremque enim facilis natus sed et?',
                        link:'',
                        tech:[
                            'test',
                            'test',
                            'test',
                        ],
                    },
                    {
                        cover:'https://upload.wikimedia.org/wikipedia/commons/thumb/1/15/Cat_August_2010-4.jpg/1200px-Cat_August_2010-4.jpg',
                        title:'Cat Proj',                        
                        description:'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Aperiam necessitatibus rerum molestiae cum itaque sint natus, mollitia nostrum ratione dolores. Ea nihil at a doloremque enim facilis natus sed et?',
                        link:'',
                        tech:[
                            'test',
                            'test',
                            'test',
                        ],
                    },
                ]
            }
        }
    }

</script>