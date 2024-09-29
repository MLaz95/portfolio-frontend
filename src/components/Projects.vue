<template>
    <section id="projects">
        <p class="section__text">Browse Some of My</p>
        <h1 class="title">Projects</h1>

        <div class="projects-container">
            <div v-for="proj in projects" class="project-card">
                
                <swiper
                :modules="modules"
                :slides-per-view="1"
                :loop="true"
                :pagination="{
                    clickable: 'true',
                }"
                >
                    <swiper-slide v-for="img in proj.covers">
                        <img class="project-cover" :src="`/src/assets/`+ img" alt="">
                    </swiper-slide>

                </swiper>


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

    .swiper{
        min-width: 100%;
        max-width: 0px;
        z-index: 0;
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
        gap: 1rem;
        padding: 0.5rem 0;
    }

    .project-info h2{
        font-size: 1.5rem;
    }

    .tech-container{
        display: flex;
        gap: 0.5rem;
        /* margin: 1rem 0; */
        overflow-x: auto;
    }

    .tech{
        font-size: 0.75rem;
        padding: 0 0.5rem;
        border: 1px solid gray;
        border-radius: 0.5rem;
        white-space: nowrap;
    }



    .project-info h2{
        text-align: center
    }

</style>

<script>
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';
import 'swiper/css/pagination';
// import 'swiper/css/navigation';
import { Pagination, Navigation } from 'swiper/modules';


    export default{
        components:{
            Swiper,
            SwiperSlide,
        },

        data(){
            return{
                projects:[
                    {
                        covers:[
                            'deliveboo-home.png',
                            'deliveboo-menu.png',
                            'deliveboo-pay.png',
                            'deliveboo-plates.png',
                        ],
                        title:'Deliveboo',                        
                        description:'Deliveboo is a mock food delivery website where customers can order food, while restaurateurs can sign up to manage their restaurant’s offerings on a back-office. Deliveboo was developed in 3 weeks in an agile group of 5 for a capstone project.',
                        link:'',
                        tech:[
                            'Laravel',
                            'Vue',
                            'PHP',
                            'JavaScript',
                            'Braintree API'
                        ],
                    },
                    {
                        covers:[
                            'boolflix-search.png',
                            'boolflix-filter.png',
                            'boolflix-info.png',
                        ],
                        title:'Movie Search',                        
                        description:'A search tool that allows the user to look for a movie or tv show from The Movie Database (TMDB). Results can then be further filtered by selecting an available genre category. This site was developed solo in a day.',
                        link:'',
                        tech:[
                            'Vue',
                            'JavaScript',
                            'TMDB API',
                        ],
                    },
                    {
                        covers:[
                            'whatsapp-home.png',
                            'whatsapp-chat.png',

                        ],
                        title:'Whatsapp Web Layout Clone',                        
                        description:'One of my earliest Vue projects! The user can filter and manage their contact list. Also whenever a message is sent each contact replies with a random cat fact! This project was developed solo over the course of an afternoon.',
                        link:'',
                        tech:[
                            'Vue',
                            'JavaScript',
                        ],
                    },
                ],

                modules: [Pagination]
            }
        }
    }

</script>