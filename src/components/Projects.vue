<template>
    <section id="projects" ref="projects" class="scroll-mt-16 lg:scroll-mt-24">
        <div>
            <ul class="group/list">
                <li v-for="(project, idx) in projects" :key="idx" class="mb-12">
                    <projects-item :item="project" />
                </li>
            </ul>
        </div>
    </section>
</template>

<script>
import ProjectsItem from '@/components/ProjectsItem.vue';

export default {
    name: 'AppProjects',
    components: {ProjectsItem},
    computed: {
        projects () {
            return [
                {
                    name: 'Meetups service',
                    description: 'Web app for planning offline meetups. View meetups, create meetups, join meetups, detailed information and meetup agenda. Authentication, calendar view of meetups and more.',
                    image: '/src/assets/images/meetups.png',
                    link: 'https://meetup-service.netlify.app/'
                },
                {
                    name: 'Crypto dashboard',
                    description: 'Crypto dashboard - check cryptocurrencies prices in real time.',
                    image: '/src/assets/images/cryptonomicon.png',
                    link: 'https://leafy-valkyrie-e1ccfa.netlify.app/'
                },
                {
                    name: 'Kanban board',
                    description: 'Kanban board - simple scrum board to plan sprints with your team!',
                    image: '/src/assets/images/kanban-board.png',
                    link: 'https://kanban-board123.netlify.app/'
                }
            ]
        }
    }
}
</script>

<style scoped>

</style>
