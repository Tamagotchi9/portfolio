<template>
  <section id="projects" ref="projects" class="scroll-mt-16 lg:scroll-mt-24">
    <h3 class="block lg:hidden font-semibold text-2xl text-slate-200 mb-3">Projects</h3>
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
import ProjectsItem from '@/components/ProjectsItem.vue'
import meetupsThumbnail from '@/assets/images/meetups.png'
import cryptoThumbnail from '@/assets/images/cryptonomicon.png'
import kanbanThumbnail from '@/assets/images/kanban-board.png'

export default {
  name: 'AppProjects',
  components: { ProjectsItem },
  computed: {
    projects() {
      return [
        {
          name: 'Meetups service',
          description:
            'Web app for planning offline meetups. View meetups, create meetups, join meetups, detailed information and meetup agenda. Authentication, calendar view of meetups and more.',
          image: meetupsThumbnail,
          link: 'https://meetup-service.netlify.app/'
        },
        {
          name: 'Crypto dashboard',
          description: 'Crypto dashboard - check cryptocurrencies prices in real time.',
          image: cryptoThumbnail,
          link: 'https://leafy-valkyrie-e1ccfa.netlify.app/'
        },
        {
          name: 'Kanban board',
          description: 'Kanban board - simple scrum board to plan sprints with your team!',
          image: kanbanThumbnail,
          link: 'https://kanban-board123.netlify.app/'
        }
      ]
    }
  }
}
</script>

<style scoped></style>
