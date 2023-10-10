<template>
    <nav class="nav hidden lg:block">
        <ul class="mt-16 w-max">
            <li>
                <a class="group flex items-center py-3 active" href="#about">
                  <span
                          class="nav-indicator mr-4 h-px transition-all group-hover:w-16 group-hover:bg-slate-200 group-focus-visible:w-16 group-focus-visible:bg-slate-200 motion-reduce:transition-none"
                          :class="{ 'w-16 bg-slate-200': active === 'about', 'w-8 bg-slate-600': active !== 'about' }"
                  ></span>
                    <span
                            class="nav-text text-xs font-bold uppercase tracking-widest group-hover:text-slate-200 group-focus-visible:text-slate-200"
                            :class="{ 'text-slate-200': active === 'about', 'text-slate-500': active !== 'about' }"
                    >About</span
                    >
                </a>
            </li>
            <li>
                <a class="group flex items-center py-3 active" href="#experience">
                  <span
                          class="nav-indicator mr-4 h-px transition-all group-hover:w-16 group-hover:bg-slate-200 group-focus-visible:w-16 group-focus-visible:bg-slate-200 motion-reduce:transition-none"
                          :class="{ 'w-16 bg-slate-200': active === 'experience', 'w-8 bg-slate-600': active !== 'experience' }"
                  ></span>
                    <span
                            class="nav-text text-xs font-bold uppercase tracking-widest group-hover:text-slate-200 group-focus-visible:text-slate-200"
                            :class="{ 'text-slate-200': active === 'experience', 'text-slate-500': active !== 'experience' }"
                    >Experience</span
                    >
                </a>
            </li>
            <li>
                <a class="group flex items-center py-3 active" href="#projects">
                  <span
                          class="nav-indicator mr-4 h-px transition-all group-hover:w-16 group-hover:bg-slate-200 group-focus-visible:w-16 group-focus-visible:bg-slate-200 motion-reduce:transition-none"
                          :class="{ 'w-16 bg-slate-200': active === 'projects', 'w-8 bg-slate-600': active !== 'projects' }"
                  ></span>
                    <span
                            class="nav-text text-xs font-bold uppercase tracking-widest group-hover:text-slate-200 group-focus-visible:text-slate-200"
                            :class="{ 'text-slate-200': active === 'projects', 'text-slate-500': active !== 'projects' }"
                    >Projects</span
                    >
                </a>
            </li>
        </ul>
    </nav>
</template>

<script>
export default {
    name: 'AppNavigation',
    props: {
        active: {
            type: String,
            default: ''
        }
    }
}
</script>

<style scoped>

</style>
