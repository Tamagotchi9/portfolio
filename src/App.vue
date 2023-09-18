<template>
  <div class="group/spotlight relative">
    <div
      class="pointer-events-none fixed inset-0 z-30 transition duration-300 lg:absolute"
      :style="bg"
    ></div>
    <Resume />
  </div>
</template>

<script>
import { defineComponent } from 'vue'
import Resume from '@/pages/Resume.vue'

export default defineComponent({
  name: 'App',
  components: {
    Resume
  },
  data() {
    return {
      x: 0,
      y: 0
    }
  },
  computed: {
    bg() {
      return {
        background: `radial-gradient(600px at ${this.x}px ${this.y}px, rgba(29,78,216, 0.15), transparent 80%)`
      }
    }
  },
  mounted() {
    document.addEventListener('mousemove', this.setMousePos)
  },
  unmounted() {
    document.removeEventListener('mousemove', this.setMousePos)
  },
  methods: {
    setMousePos(event) {
      this.x = event.pageX
      this.y = event.pageY
    }
  }
})
</script>

<style scoped lang="scss"></style>
