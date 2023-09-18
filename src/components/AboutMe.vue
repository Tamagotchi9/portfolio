<template>
  <section class="py-20">
    <div class="container mx-auto">
      <div class="flex items-center justify-center gap-5">
        <div class="h-full w-6/12">
          <p class="font-mono text-lg">
            I have been working as a FrontEnd Developer for 3 years. I'm responsible person who
            ready for challenges. I'm always curios about optimized, readable and elegant solutions.
            I like to do sports in my free time, especially snowboarding, basketball, crossfit.
          </p>
          <div class="mt-4">
            <p class="font-mono font-bold italic text-2xl pb-3">Experience</p>
            <ol class="relative border-l border-gray-200 dark:border-gray-700">
              <li class="mb-10 ml-4">
                <div
                  class="absolute w-3 h-3 bg-gray-200 rounded-full mt-1.5 -left-1.5 border border-white dark:border-gray-900 dark:bg-gray-700"
                ></div>
                <time class="mb-1 text-sm font-normal leading-none text-gray-400 dark:text-gray-500"
                  >October 2022 - Present</time
                >
                <h3 class="text-lg font-semibold text-gray-900 dark:text-white">
                  FrontEnd developer
                </h3>
                <h4 class="text-md font-semibold text-gray-700 dark:text-white">Checkbox</h4>
                <p class="mb-4 text-base font-normal text-gray-500 dark:text-gray-400">
                  Working as Vue Dev
                </p>
              </li>
              <li class="mb-10 ml-4">
                <div
                  class="absolute w-3 h-3 bg-gray-200 rounded-full mt-1.5 -left-1.5 border border-white dark:border-gray-900 dark:bg-gray-700"
                ></div>
                <time class="mb-1 text-sm font-normal leading-none text-gray-400 dark:text-gray-500"
                  >October 2021 - November 2022</time
                >
                <h3 class="text-lg font-semibold text-gray-900 dark:text-white">
                  Middle FrontEnd developer
                </h3>
                <h4 class="text-md font-semibold text-gray-700 dark:text-white">Valtech</h4>
                <p class="text-base font-normal text-gray-500 dark:text-gray-400">
                  Working as Vue Dev
                </p>
              </li>
              <li class="ml-4">
                <div
                  class="absolute w-3 h-3 bg-gray-200 rounded-full mt-1.5 -left-1.5 border border-white dark:border-gray-900 dark:bg-gray-700"
                ></div>
                <time class="mb-1 text-sm font-normal leading-none text-gray-400 dark:text-gray-500"
                  >July 2020 - October 2021</time
                >
                <h3 class="text-lg font-semibold text-gray-900 dark:text-white">
                  Junior FrontEnd developer
                </h3>
                <h4 class="text-md font-semibold text-gray-700 dark:text-white">Beyond.GG</h4>
                <p class="text-base font-normal text-gray-500 dark:text-gray-400">
                  As a part of FrontEnd team, I delivered a lot of UI pages from scratch, built
                  modules
                </p>
              </li>
            </ol>
          </div>
        </div>
        <div class="w-6/12">
          <div class="flex items-center justify-center">
            <div class="max-w-xs rounded-xl">
              <img class="rounded-xl" src="@/assets/images/me.jpg" alt="me" />
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'AboutMe'
}
</script>

<style scoped lang="scss"></style>
