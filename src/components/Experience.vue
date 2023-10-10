<template>
    <section
        id="experience"
        ref="experience"
        class="mb-16 scroll-mt-16 md:mb-24 lg:mb-36 lg:scroll-mt-24"
        aria-label="Work experience"
    >
        <div>
            <ol class="group/list">
                <li v-for="(expItem, idx) in experience" :key="idx" class="mb-12">
                    <experience-item :item="expItem" />
                </li>
            </ol>
            <div class="mt-12">
                <a
                    href=""
                    class="inline-flex items-center font-medium leading-tight text-slate-200 font-semibold text-slate-200 group"
                    aria-label="View Full Resume"
                >
                    <span
                        class="border-b border-transparent pb-px transition group-hover:border-teal-300 motion-reduce:transition-none"
                        >View Full Resume</span
                    >
                    <component
                        :is="arrowRightIcon"
                        class="ml-1 inline-block h-4 w-4 shrink-0 -translate-y-px transition-transform group-hover:translate-x-2 group-focus-visible:translate-x-2 motion-reduce:transition-none"
                    />
                </a>
            </div>
        </div>
    </section>
</template>

<script>
import ExperienceItem from '@/components/ExperienceItem.vue';
import { ArrowRightIcon } from '@heroicons/vue/24/outline'

export default {
    name: 'AppExperience',
    components: {ExperienceItem},
    computed: {
        experience () {
            return [
                {
                    date: '2022 October - Present',
                    position: 'FrontEnd Developer',
                    description: 'Built fast, high-quality and robust production code for new services like Navkolo, Navkolo Edo for online documents signing, implemented bunch of features on main product Checkbox.',
                    technologies: ['Nuxt', 'Vuex', 'VuexORM', 'Vuetify', 'VeeValidate', 'Javascript', 'SCSS', 'Jest'],
                    link: 'https://checkbox.ua/'
                },
                {
                    date: '2021 September - 2022 October',
                    position: 'FrontEnd Developer',
                    description: 'Developed and styled interactive web pages for e-health HARTMANN ecommerce platform. Built many sections of product like checkout, shopping cart, refactored code for readability and reduced components dependencies.',
                    technologies: ['Vue.js', 'Bootstrap 4', 'Vuelidate', 'Javascript', 'SCSS', 'Storybook'],
                    link: 'https://www.valtech.com/?utm_source=google&utm_medium=cpc&utm_campaign=UA_branding&utm_term=brand_Brand_Search-UA&utm_content=awareness_other_search-ad_brand_week47-2022&gclid=CjwKCAjw_uGmBhBREiwAeOfsd6EZ-YdbJyGfUkV3lMAU7ZGHUvUN2Mt7K1IgLXcoRMRtR7NKtpJokRoCdIIQAvD_BwE'
                },
                {
                    date: '2020 August - 2021 September',
                    position: 'FrontEnd Developer',
                    description: 'Built customize UI pages for SaaS e-gaming platform, solving unusual tasks, handling data in Vuex, built generic components for future use-cases.',
                    technologies: ['Vue.js', 'Vuex', 'Vuelidate', 'Javascript', 'SCSS'],
                    link: 'https://beyondindustries.io/'
                }
            ]
        },
        arrowRightIcon() {
            return ArrowRightIcon
        }
    }
}
</script>

<style scoped></style>
