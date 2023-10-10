<template>
    <div
        class="group relative grid pb-1 transition-all sm:grid-cols-8 sm:gap-8 md:gap-4 lg:hover:!opacity-100 lg:group-hover/list:opacity-50"
    >
        <div
            class="absolute -inset-x-4 -inset-y-4 z-0 hidden rounded-md transition motion-reduce:transition-none lg:-inset-x-6 lg:block lg:group-hover:bg-slate-800/50 lg:group-hover:shadow-[inset_0_1px_0_0_rgba(148,163,184,0.1)] lg:group-hover:drop-shadow-lg"
        ></div>
        <header
            class="z-10 mb-2 mt-1 text-xs font-semibold uppercase tracking-wide text-slate-500 sm:col-span-2"
            aria-label="2022 - Present"
        >
            {{ item.date }}
        </header>
        <div class="z-10 sm:col-span-6">
            <h3 class="font-medium leading-snug text-slate-200">
                <a
                    class="inline-flex items-baseline font-medium leading-tight text-slate-200 hover:text-teal-300 focus-visible:text-teal-300 group/link text-base"
                    href="https://checkbox.ua/"
                    target="_blank"
                    rel="noreferrer"
                    aria-label="FrontEnd developer at Checkbox"
                >
                    <span
                        class="absolute -inset-x-4 -inset-y-2.5 hidden rounded md:-inset-x-6 md:-inset-y-4 lg:block"
                    ></span>
                    <span>
                        {{ item.position }} -
                        <span class="inline-block">
                            Checkbox
                            <component
                                :is="arrowUpRightIcon"
                                class="inline-block h-4 w-4 shrink-0 transition-transform group-hover/link:-translate-y-1 group-hover/link:translate-x-1 group-focus-visible/link:translate-x-1 motion-reduce:transition-none ml-1 translate-y-px"
                            />
                        </span>
                    </span>
                </a>
            </h3>
            <p class="mt-2 text-sm leading-normal">
                {{ item.achievements }}
            </p>
            <ul class="mt-2 flex flex-wrap" aria-label="Technologies used">
                <li v-for="(tech,idx) in item.technologies" :key="idx" class="mr-1.5 mt-2">
                    <div
                        class="flex items-center rounded-full bg-teal-400/10 px-3 py-1 text-xs font-medium leading-5 text-teal-300"
                    >
                        {{ tech }}
                    </div>
                </li>
            </ul>
        </div>
    </div>
</template>

<script>
import { ArrowUpRightIcon } from '@heroicons/vue/24/outline'

export default {
    name: 'ExperienceItem',
    props: {
        item: {
            type: Object,
            default: null
        }
    },
    computed: {
        arrowUpRightIcon() {
            return ArrowUpRightIcon
        },
    }
}
</script>

<style scoped>

</style>
