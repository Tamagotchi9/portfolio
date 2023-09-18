<template>
  <header class="w-full h-20 fixed border-blue-500 border-b bg-white">
    <nav class="h-full">
      <ul class="h-full flex justify-center items-center gap-x-3">
        <li>
          <a href="">About me</a>
        </li>
        <li>
          <a href="">Portfolio</a>
        </li>
        <li>
          <a href="">Career</a>
        </li>
        <li>
          <a href="">Contacts</a>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'AppHeader'
})
</script>

<style scoped lang="scss"></style>
