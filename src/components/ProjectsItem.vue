<template>
    <div
            class="group relative grid gap-4 pb-1 transition-all sm:grid-cols-8 sm:gap-8 md:gap-4 lg:hover:!opacity-100 lg:group-hover/list:opacity-50"
    >
        <div
                class="absolute -inset-x-4 -inset-y-4 z-0 hidden rounded-md transition motion-reduce:transition-none lg:-inset-x-6 lg:block lg:group-hover:bg-slate-800/50 lg:group-hover:shadow-[inset_0_1px_0_0_rgba(148,163,184,0.1)] lg:group-hover:drop-shadow-lg"
        ></div>
        <div class="z-10 sm:order-2 sm:col-span-6">
            <h3>
                <a
                        class="inline-flex items-baseline font-medium leading-tight text-slate-200 hover:text-teal-300 focus-visible:text-teal-300 group/link text-base"
                        :href="item.link"
                        target="_blank"
                        rel="noreferrer"
                        aria-label="Meetups service"
                >
                        <span
                                class="absolute -inset-x-4 -inset-y-2.5 hidden rounded md:-inset-x-6 md:-inset-y-4 lg:block"
                        ></span>
                    <span>
                          {{ item.name }}
                          <component
                                  :is="arrowUpRightIcon"
                                  class="inline-block h-4 w-4 shrink-0 transition-transform group-hover/link:-translate-y-1 group-hover/link:translate-x-1 group-focus-visible/link:translate-x-1 motion-reduce:transition-none ml-1 translate-y-px"
                          />
                        </span>
                </a>
            </h3>
            <p class="mt-2 text-sm leading-normal">
                {{ item.description }}
            </p>
        </div>
        <img
                class="rounded border-2 border-slate-200/10 transition group-hover:border-slate-200/30 sm:order-1 sm:col-span-2 sm:translate-y-1 sm:max-h-18"
                loading="lazy"
                width="200"
                height="48"
                decoding="async"
                :src="item.image"
                alt="meetups-cover"
        />
    </div>
</template>

<script>
import { ArrowUpRightIcon } from '@heroicons/vue/24/outline'

export default {
    name: 'ProjectsItem',
    props: {
        item: {
            type: Object,
            default: null
        }
    },
    computed: {
        arrowUpRightIcon() {
            return ArrowUpRightIcon
        }
    }
}
</script>

<style scoped>

</style>
