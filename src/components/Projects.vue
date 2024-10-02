<template>
    <section id="projects">
        <p class="section__text">Browse Some of My</p>
        <h1 class="title">Projects</h1>

        <div class="projects-container">
            <div v-for="proj in projects" class="project-card">
                <h2>{{ proj.title }}</h2>
                
                <swiper
                :modules="modules"
                :slides-per-view="1"
                :loop="true"
                :pagination="{
                    clickable: 'true',
                }"
                >
                    <swiper-slide v-for="img in proj.covers">
                        <img class="project-cover" :src="`/img/` + img" alt="">
                    </swiper-slide>

                </swiper>


                <div class="project-info">
                    <div class="tech-container">
                        <div v-for="tech in proj.tech" class="tech">{{ tech }}</div>
                    </div>
                    <p>
                        {{ proj.description }}
                    </p>
                    <div class="btn-container">
                        <a :href="proj.link" target="_blank"><button class="btn btn-color-1">Github</button></a>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<style>

    section#projects{
        height: 100%;
        margin: 0;
    }

    .projects-container{
        display: flex;
        flex-direction: column;
        gap: 2rem;

        max-width: 800px;
        margin: 3rem auto 0 auto;
    }

    .projects-container a{
        text-align: center;
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

    .project-card h2{
        text-align: center;
        margin-bottom: 1rem;
    }

    .swiper{
        min-width: 100%;
        max-width: 0px;
        z-index: 0;
    }

    .swiper-pagination-bullet-active{
        background-color: var(--highlight);
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
        text-align: center;
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
                            'deliveboo-hero.png',
                            'deliveboo-home.png',
                            'deliveboo-menu.png',
                            'deliveboo-pay.png',
                            'deliveboo-plates.png',
                        ],
                        title:'Deliveboo',                        
                        description:'Deliveboo is a mock food delivery website. Customers can filter restaurants through categories and add food items to their cart off of a chosen restaurant’s menu. They can then review their order and complete their purchase by adding delivery information and a valid credit card. Restauranteurs can sign up to feature their restaurant on the site and get access to a back-office where they have access to order metrics and can manage which dishes are available. Deliveboo was developed in 3 weeks in an agile group of 5 for a capstone project.',
                        link:'https://github.com/MLaz95/deliveboo-backoffice',
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
                        description:'A simple search tool that allows the user to look for a movie or tv show from The Movie Database (TMDB). The search results can then be further filtered by selecting an available genre category. Each result displays a plot summary, genre tags, and a main cast list. This site was developed solo in a day.',
                        link:'https://github.com/MLaz95/vite-boolflix',
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
                        description:'This is a clone of a whatsapp web interface and one of my earliest Vue projects! The user can filter contacts by name, and delete one or add a new one. Each chat history can also be deleted, either entirely or message by message. Also when a message is sent each contact replies with a random cat fact! This project was developed solo over the course of an afternoon.',
                        link:'https://github.com/MLaz95/vue-boolzapp',
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