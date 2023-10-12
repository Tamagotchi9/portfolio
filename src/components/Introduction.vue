<template>
  <header class="lg:w-1/2 static lg:sticky lg:top-0 lg:max-h-screen flex flex-col justify-between lg:py-24">
    <div>
        <div class="flex flex-col items-center lg:flex-row lg:items-start">
            <div class="rounded-full w-24 h-24 border-slate-200 border-2 mr-4">
                <img class="rounded-full w-full h-auto"  src="../assets/thumbnail.jpeg" alt="me">
            </div>
            <div>
                <h1 class="text-4xl font-bold text-slate-200 tracking-tight sm:text-5xl">
                    Dmytro Voloshko
                </h1>
                <h2 class="mt-3 text-xl font-medium tracking-tight text-slate-200 sm:text-xl">
                    Frontend Developer at Checkbox
                </h2>
                <p class="mt-4 max-w-xs leading-normal">
                    Frontend enthusiast, constantly growing, delivering great UI experience.
                </p>
            </div>
        </div>
      <navigation :active="active"/>
    </div>
    <social/>
  </header>
</template>

<script>
import { defineComponent } from 'vue'
import Navigation from '@/components/Navigation.vue';
import Social from '@/components/Social.vue'

export default defineComponent({
  name: 'AppIntroduction',
    props: {
      active: {
        type: String,
        default: ''
      }
    },
  components: {
    Navigation,
    Social
  }
})
</script>

<style lang="scss">
</style>
