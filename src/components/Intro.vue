<template>
  <section class="h-screen flex items-center justify-center">
    <div class="container mx-auto">
      <div class="columns-1">
        <div class="text-center max-w-2xl mx-auto">
          <animated-title />
          <button
            class="bg-blue-700 text-zinc-50 px-10 py-4 font-sans text-lg font-medium rounded-lg mt-5"
          >
            About me
          </button>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import { defineComponent } from 'vue'
import AnimatedTitle from '@/components/AnimatedTitle.vue'

export default defineComponent({
  name: 'AppIntro',
  components: { AnimatedTitle }
})
</script>

<style lang="scss">
.slide-in-enter-active,
.slide-in-leave-active {
  transition: opacity 0.5s ease;
}

.slide-in-enter-from,
.slide-in-leave-to {
  opacity: 0;
}
.slide-in-enter-to,
.slide-in-leave-form {
  opacity: 1;
}
</style>
