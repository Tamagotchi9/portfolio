<template>
  <div
    class="mx-auto min-h-screen max-w-screen-xl px-6 py-12 font-sans md:px-12 md:py-20 lg:px-24 lg:py-0"
  >
    <div class="flex flex-col lg:flex-row justify-between gap-4">
      <Introduction :active="activeArea"/>
      <main id="content" class="pt-16 lg:w-1/2 lg:py-24">
        <about-me ref="aboutSection"/>
        <experience ref="experienceSection"/>
        <projects ref="projectsSection"/>
      </main>
    </div>
  </div>
</template>

<script>
import { defineComponent } from 'vue'
import Introduction from '@/components/Introduction.vue';
import AboutMe from '@/components/AboutMe.vue';
import Experience from '@/components/Experience.vue';
import Projects from '@/components/Projects.vue';

export default defineComponent({
  name: 'AppResume',
  components: {
    Introduction,
    AboutMe,
    Experience,
      Projects
  },
  data () {
    return {
      activeArea: 'about'
    }
  },
  mounted () {
    window.addEventListener('scroll', this.handleScroll)
  },
  unmounted () {
    window.removeEventListener('scroll', this.handleScroll)
  },
  methods: {
    handleScroll () {
      const aboutSection = this.$refs.aboutSection.$refs.about
      const experienceSection = this.$refs.experienceSection.$refs.experience
      const projectsSection = this.$refs.projectsSection.$refs.projects
      let scrollY = window.scrollY;

      [aboutSection, experienceSection, projectsSection].forEach(current => {
        const sectionHeight = current.offsetHeight;
        const sectionTop = current.offsetTop - 300;
        console.log(current.offsetHeight)
        // console.log('scrollY', scrollY)
        // console.log(sectionTop, sectionHeight)
        if (
          scrollY > sectionTop &&
          scrollY <= sectionHeight + sectionTop
        ){
          this.activeArea = current.id
        }
      });
    }
  }
})
</script>

<style scoped lang="scss"></style>
