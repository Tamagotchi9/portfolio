<template>
  <div
    class="mx-auto min-h-screen max-w-screen-xl px-6 py-12 font-sans md:px-12 md:py-20 lg:px-24 lg:py-0"
  >
    <div class="flex justify-between gap-4">
      <header class="w-1/2 sticky top-0 max-h-screen flex flex-col justify-between py-24">
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
          <nav class="nav hidden lg:block">
            <ul class="mt-16 w-max">
              <li>
                <a class="group flex items-center py-3 active" href="#about">
                  <span
                    class="nav-indicator mr-4 h-px w-8 bg-slate-600 transition-all group-hover:w-16 group-hover:bg-slate-200 group-focus-visible:w-16 group-focus-visible:bg-slate-200 motion-reduce:transition-none"
                    :class="{ 'w-16 bg-slate-200': activeArea === 'about', 'w-8 bg-slate-600': activeArea !== 'about' }"
                  ></span>
                  <span
                    class="nav-text text-xs font-bold uppercase tracking-widest group-hover:text-slate-200 group-focus-visible:text-slate-200"
                    :class="{ 'text-slate-200': activeArea === 'about', 'text-slate-500': activeArea !== 'about' }"
                    >About</span
                  >
                </a>
              </li>
              <li>
                <a class="group flex items-center py-3 active" href="#experience">
                  <span
                    class="nav-indicator mr-4 h-px transition-all group-hover:w-16 group-hover:bg-slate-200 group-focus-visible:w-16 group-focus-visible:bg-slate-200 motion-reduce:transition-none"
                    :class="{ 'w-16 bg-slate-200': activeArea === 'experience', 'w-8 bg-slate-600': activeArea !== 'experience' }"
                  ></span>
                  <span
                    class="nav-text text-xs font-bold uppercase tracking-widest group-hover:text-slate-200 group-focus-visible:text-slate-200"
                    :class="{ 'text-slate-200': activeArea === 'experience', 'text-slate-500': activeArea !== 'experience' }"
                    >Experience</span
                  >
                </a>
              </li>
              <li>
                <a class="group flex items-center py-3 active" href="#projects">
                  <span
                    class="nav-indicator mr-4 h-px transition-all group-hover:w-16 group-hover:bg-slate-200 group-focus-visible:w-16 group-focus-visible:bg-slate-200 motion-reduce:transition-none"
                    :class="{ 'w-16 bg-slate-200': activeArea === 'projects', 'w-8 bg-slate-600': activeArea !== 'projects' }"
                  ></span>
                  <span
                    class="nav-text text-xs font-bold uppercase tracking-widest group-hover:text-slate-200 group-focus-visible:text-slate-200"
                    :class="{ 'text-slate-200': activeArea === 'projects', 'text-slate-500': activeArea !== 'projects' }"
                    >Projects</span
                  >
                </a>
              </li>
            </ul>
          </nav>
        </div>
        <ul class="ml-1 mt-8 flex items-center">
          <li class="mr-5 text-xs">
            <a
              class="block hover:text-slate-200"
              href="https://github.com/Tamagotchi9"
              target="_blank"
              rel="noreferrer"
            >
              <span class="sr-only">Github</span>
              <svg
                class="fill-slate-100"
                xmlns="http://www.w3.org/2000/svg"
                width="24"
                height="24"
                viewBox="0 0 24 24"
              >
                <path
                  d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"
                />
              </svg>
            </a>
          </li>
          <li class="mr-5 text-xs">
            <a
              class="block hover:text-slate-200"
              href="https://www.instagram.com/dimavoloshko_9/"
              target="_blank"
              rel="noreferrer"
            >
              <span class="sr-only">Instagram</span>
              <svg
                class="fill-slate-100"
                xmlns="http://www.w3.org/2000/svg"
                width="24"
                height="24"
                viewBox="0 0 24 24"
              >
                <path
                  d="M11.984 16.815c2.596 0 4.706-2.111 4.706-4.707 0-1.409-.623-2.674-1.606-3.538-.346-.303-.735-.556-1.158-.748-.593-.27-1.249-.421-1.941-.421s-1.349.151-1.941.421c-.424.194-.814.447-1.158.749-.985.864-1.608 2.129-1.608 3.538 0 2.595 2.112 4.706 4.706 4.706zm.016-8.184c1.921 0 3.479 1.557 3.479 3.478 0 1.921-1.558 3.479-3.479 3.479s-3.479-1.557-3.479-3.479c0-1.921 1.558-3.478 3.479-3.478zm5.223.369h6.777v10.278c0 2.608-2.114 4.722-4.722 4.722h-14.493c-2.608 0-4.785-2.114-4.785-4.722v-10.278h6.747c-.544.913-.872 1.969-.872 3.109 0 3.374 2.735 6.109 6.109 6.109s6.109-2.735 6.109-6.109c.001-1.14-.327-2.196-.87-3.109zm2.055-9h-12.278v5h-1v-5h-1v5h-1v-4.923c-.346.057-.682.143-1 .27v4.653h-1v-4.102c-1.202.857-2 2.246-2 3.824v3.278h7.473c1.167-1.282 2.798-2 4.511-2 1.722 0 3.351.725 4.511 2h7.505v-3.278c0-2.608-2.114-4.722-4.722-4.722zm2.722 5.265c0 .406-.333.735-.745.735h-2.511c-.411 0-.744-.329-.744-.735v-2.53c0-.406.333-.735.744-.735h2.511c.412 0 .745.329.745.735v2.53z"
                />
              </svg>
            </a>
          </li>
          <li class="text-xs">
            <a
              class="block hover:text-slate-200"
              href="https://www.linkedin.com/in/dima-voloshko-660922130/"
              target="_blank"
              rel="noreferrer"
            >
              <span class="sr-only">Linkedin</span>
              <svg
                class="fill-slate-100"
                xmlns="http://www.w3.org/2000/svg"
                width="24"
                height="24"
                viewBox="0 0 24 24"
              >
                <path
                  d="M4.98 3.5c0 1.381-1.11 2.5-2.48 2.5s-2.48-1.119-2.48-2.5c0-1.38 1.11-2.5 2.48-2.5s2.48 1.12 2.48 2.5zm.02 4.5h-5v16h5v-16zm7.982 0h-4.968v16h4.969v-8.399c0-4.67 6.029-5.052 6.029 0v8.399h4.988v-10.131c0-7.88-8.922-7.593-11.018-3.714v-2.155z"
                />
              </svg>
            </a>
          </li>
        </ul>
      </header>
      <main id="content" class="pt-24 lg:w-1/2 lg:py-24">
        <section
          id="about"
          ref="about"
          class="mb-16 scroll-mt-16 md:mb-24 lg:mb-36 lg:scroll-mt-24"
          aria-label="About me"
        >
          <div>
            <p class="mb-4">
              Back in 2017, in the last term of school, I decided to start picking up web
              development. I had a lot of ups and downs when I was learning front-end, but
              fast-forward to today, and I've had experience of building software for a
              <a
                href="https://beyondindustries.io/"
                target="_blank"
                rel="noreferrer"
                class="font-medium text-slate-200 hover:text-teal-300 focus-visible:text-teal-300"
                >SaaS product</a
              >, an
              <a
                href="https://www.hartmann.info/"
                target="_blank"
                rel="noreferrer"
                class="font-medium text-slate-200 hover:text-teal-300 focus-visible:text-teal-300"
                >e-health ecommerce shop</a
              >, a
              <a
                href="https://checkbox.ua/"
                target="_blank"
                rel="noreferrer"
                class="font-medium text-slate-200 hover:text-teal-300 focus-visible:text-teal-300"
                >Ukrainian fintech product</a
              >.
            </p>
            <p class="mb-4">
              Currently I'm working at
              <a
                href="https://checkbox.ua/"
                target="_blank"
                rel="noreferrer"
                class="font-medium text-slate-200 hover:text-teal-300 focus-visible:text-teal-300"
                >Checkbox</a
              >, where I'm building UI of products which are used by Ukrainian businesses.
            </p>
            <p>
              When I'm not at the computer, I'm usually do sports (cause I'm a big fan of it,
              especially crossfit, basketball, swimming, hiking) or hanging out with girlfriend or
              friends.
            </p>
          </div>
        </section>
        <section
          id="experience"
          ref="experience"
          class="mb-16 scroll-mt-16 md:mb-24 lg:mb-36 lg:scroll-mt-24"
          aria-label="Work experience"
        >
          <div>
            <ol class="group/list">
              <li class="mb-12">
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
                    2022 October - Present
                  </header>
                  <div class="z-10 sm:col-span-6">
                    <h3 class="font-medium leading-snug text-slate-200">
                      <div>
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
                            FrontEnd Developer -
                            <span class="inline-block">
                              Checkbox
                              <component
                                :is="arrowUpRightIcon"
                                class="inline-block h-4 w-4 shrink-0 transition-transform group-hover/link:-translate-y-1 group-hover/link:translate-x-1 group-focus-visible/link:translate-x-1 motion-reduce:transition-none ml-1 translate-y-px"
                              />
                            </span>
                          </span>
                        </a>
                      </div>
                    </h3>
                    <p class="mt-2 text-sm leading-normal">
                      Built fast, high-quality and robust production code for new services like
                      Navkolo, Navkolo Edo for online documents signing, implemented bunch of
                      features on main product Checkbox.
                    </p>
                    <ul class="mt-2 flex flex-wrap" aria-label="Technologies used">
                      <li class="mr-1.5 mt-2">
                        <div
                          class="flex items-center rounded-full bg-teal-400/10 px-3 py-1 text-xs font-medium leading-5 text-teal-300"
                        >
                          Nuxt
                        </div>
                      </li>
                      <li class="mr-1.5 mt-2">
                        <div
                          class="flex items-center rounded-full bg-teal-400/10 px-3 py-1 text-xs font-medium leading-5 text-teal-300"
                        >
                          Vuex
                        </div>
                      </li>
                      <li class="mr-1.5 mt-2">
                        <div
                          class="flex items-center rounded-full bg-teal-400/10 px-3 py-1 text-xs font-medium leading-5 text-teal-300"
                        >
                          VuexORM
                        </div>
                      </li>
                      <li class="mr-1.5 mt-2">
                        <div
                          class="flex items-center rounded-full bg-teal-400/10 px-3 py-1 text-xs font-medium leading-5 text-teal-300"
                        >
                          Vuetify
                        </div>
                      </li>
                      <li class="mr-1.5 mt-2">
                        <div
                          class="flex items-center rounded-full bg-teal-400/10 px-3 py-1 text-xs font-medium leading-5 text-teal-300"
                        >
                          VeeValidate
                        </div>
                      </li>
                      <li class="mr-1.5 mt-2">
                        <div
                          class="flex items-center rounded-full bg-teal-400/10 px-3 py-1 text-xs font-medium leading-5 text-teal-300"
                        >
                          Javascript
                        </div>
                      </li>
                      <li class="mr-1.5 mt-2">
                        <div
                          class="flex items-center rounded-full bg-teal-400/10 px-3 py-1 text-xs font-medium leading-5 text-teal-300"
                        >
                          SCSS
                        </div>
                      </li>
                      <li class="mr-1.5 mt-2">
                        <div
                          class="flex items-center rounded-full bg-teal-400/10 px-3 py-1 text-xs font-medium leading-5 text-teal-300"
                        >
                          Jest
                        </div>
                      </li>
                    </ul>
                  </div>
                </div>
              </li>
              <li class="mb-12">
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
                    2021 September - 2022 October
                  </header>
                  <div class="z-10 sm:col-span-6">
                    <h3 class="font-medium leading-snug text-slate-200">
                      <div>
                        <a
                          class="inline-flex items-baseline font-medium leading-tight text-slate-200 hover:text-teal-300 focus-visible:text-teal-300 group/link text-base"
                          href="https://www.valtech.com/?utm_source=google&utm_medium=cpc&utm_campaign=UA_branding&utm_term=brand_Brand_Search-UA&utm_content=awareness_other_search-ad_brand_week47-2022&gclid=CjwKCAjw_uGmBhBREiwAeOfsd6EZ-YdbJyGfUkV3lMAU7ZGHUvUN2Mt7K1IgLXcoRMRtR7NKtpJokRoCdIIQAvD_BwE"
                          target="_blank"
                          rel="noreferrer"
                          aria-label="FrontEnd developer at Checkbox"
                        >
                          <span
                            class="absolute -inset-x-4 -inset-y-2.5 hidden rounded md:-inset-x-6 md:-inset-y-4 lg:block"
                          ></span>
                          <span>
                            FrontEnd Developer -
                            <span class="inline-block">
                              Valtech
                              <component
                                :is="arrowUpRightIcon"
                                class="inline-block h-4 w-4 shrink-0 transition-transform group-hover/link:-translate-y-1 group-hover/link:translate-x-1 group-focus-visible/link:translate-x-1 motion-reduce:transition-none ml-1 translate-y-px"
                              />
                            </span>
                          </span>
                        </a>
                      </div>
                    </h3>
                    <p class="mt-2 text-sm leading-normal">
                      Developed and styled interactive web pages for e-health HARTMANN ecommerce
                      platform. Built many sections of product like checkout, shopping cart,
                      refactored code for readability and reduced components dependencies.
                    </p>
                    <ul class="mt-2 flex flex-wrap" aria-label="Technologies used">
                      <li class="mr-1.5 mt-2">
                        <div
                          class="flex items-center rounded-full bg-teal-400/10 px-3 py-1 text-xs font-medium leading-5 text-teal-300"
                        >
                          Vue.js
                        </div>
                      </li>
                      <li class="mr-1.5 mt-2">
                        <div
                          class="flex items-center rounded-full bg-teal-400/10 px-3 py-1 text-xs font-medium leading-5 text-teal-300"
                        >
                          Bootstrap 4
                        </div>
                      </li>
                      <li class="mr-1.5 mt-2">
                        <div
                          class="flex items-center rounded-full bg-teal-400/10 px-3 py-1 text-xs font-medium leading-5 text-teal-300"
                        >
                          Vuelidate
                        </div>
                      </li>
                      <li class="mr-1.5 mt-2">
                        <div
                          class="flex items-center rounded-full bg-teal-400/10 px-3 py-1 text-xs font-medium leading-5 text-teal-300"
                        >
                          Javascript
                        </div>
                      </li>
                      <li class="mr-1.5 mt-2">
                        <div
                          class="flex items-center rounded-full bg-teal-400/10 px-3 py-1 text-xs font-medium leading-5 text-teal-300"
                        >
                          SCSS
                        </div>
                      </li>
                      <li class="mr-1.5 mt-2">
                        <div
                          class="flex items-center rounded-full bg-teal-400/10 px-3 py-1 text-xs font-medium leading-5 text-teal-300"
                        >
                          Storybook
                        </div>
                      </li>
                    </ul>
                  </div>
                </div>
              </li>
              <li class="mb-12">
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
                    2020 August - 2021 September
                  </header>
                  <div class="z-10 sm:col-span-6">
                    <h3 class="font-medium leading-snug text-slate-200">
                      <div>
                        <a
                          class="inline-flex items-baseline font-medium leading-tight text-slate-200 hover:text-teal-300 focus-visible:text-teal-300 group/link text-base"
                          href="https://beyondindustries.io/"
                          target="_blank"
                          rel="noreferrer"
                          aria-label="FrontEnd developer at Checkbox"
                        >
                          <span
                            class="absolute -inset-x-4 -inset-y-2.5 hidden rounded md:-inset-x-6 md:-inset-y-4 lg:block"
                          ></span>
                          <span>
                            FrontEnd Developer -
                            <span class="inline-block">
                              Beyond
                              <component
                                :is="arrowUpRightIcon"
                                class="inline-block h-4 w-4 shrink-0 transition-transform group-hover/link:-translate-y-1 group-hover/link:translate-x-1 group-focus-visible/link:translate-x-1 motion-reduce:transition-none ml-1 translate-y-px"
                              />
                            </span>
                          </span>
                        </a>
                      </div>
                    </h3>
                    <p class="mt-2 text-sm leading-normal">
                      Built customize UI pages for SaaS e-gaming platform, solving unusual tasks,
                      handling data in Vuex, built generic components for future use-cases.
                    </p>
                    <ul class="mt-2 flex flex-wrap" aria-label="Technologies used">
                      <li class="mr-1.5 mt-2">
                        <div
                          class="flex items-center rounded-full bg-teal-400/10 px-3 py-1 text-xs font-medium leading-5 text-teal-300"
                        >
                          Vue.js
                        </div>
                      </li>
                      <li class="mr-1.5 mt-2">
                        <div
                          class="flex items-center rounded-full bg-teal-400/10 px-3 py-1 text-xs font-medium leading-5 text-teal-300"
                        >
                          Vuex
                        </div>
                      </li>
                      <li class="mr-1.5 mt-2">
                        <div
                          class="flex items-center rounded-full bg-teal-400/10 px-3 py-1 text-xs font-medium leading-5 text-teal-300"
                        >
                          Vuelidate
                        </div>
                      </li>
                      <li class="mr-1.5 mt-2">
                        <div
                          class="flex items-center rounded-full bg-teal-400/10 px-3 py-1 text-xs font-medium leading-5 text-teal-300"
                        >
                          Javascript
                        </div>
                      </li>
                      <li class="mr-1.5 mt-2">
                        <div
                          class="flex items-center rounded-full bg-teal-400/10 px-3 py-1 text-xs font-medium leading-5 text-teal-300"
                        >
                          SCSS
                        </div>
                      </li>
                    </ul>
                  </div>
                </div>
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
        <section id="projects" ref="projects" class="scroll-mt-16 lg:scroll-mt-24">
          <div>
            <ul class="group/list">
              <li class="mb-12">
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
                        href="https://meetup-service.netlify.app/"
                        target="_blank"
                        rel="noreferrer"
                        aria-label="Meetups service"
                      >
                        <span
                          class="absolute -inset-x-4 -inset-y-2.5 hidden rounded md:-inset-x-6 md:-inset-y-4 lg:block"
                        ></span>
                        <span>
                          Meetups service
                          <component
                            :is="arrowUpRightIcon"
                            class="inline-block h-4 w-4 shrink-0 transition-transform group-hover/link:-translate-y-1 group-hover/link:translate-x-1 group-focus-visible/link:translate-x-1 motion-reduce:transition-none ml-1 translate-y-px"
                          />
                        </span>
                      </a>
                    </h3>
                    <p class="mt-2 text-sm leading-normal">
                      Web app for planning offline meetups. View meetups, create meetups, join
                      meetups, detailed information and meetup agenda. Authentication, calendar view
                      of meetups and more.
                    </p>
                  </div>
                  <img
                    class="rounded border-2 border-slate-200/10 transition group-hover:border-slate-200/30 sm:order-1 sm:col-span-2 sm:translate-y-1 sm:max-h-18"
                    loading="lazy"
                    width="200"
                    height="48"
                    decoding="async"
                    src="@/assets/images/meetups.png"
                    alt="meetups-cover"
                  />
                </div>
              </li>
              <li class="mb-12">
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
                        href="https://leafy-valkyrie-e1ccfa.netlify.app/"
                        target="_blank"
                        rel="noreferrer"
                        aria-label="Crypto dashboard"
                      >
                        <span
                          class="absolute -inset-x-4 -inset-y-2.5 hidden rounded md:-inset-x-6 md:-inset-y-4 lg:block"
                        ></span>
                        <span>
                          Crypto dashboard
                          <component
                            :is="arrowUpRightIcon"
                            class="inline-block h-4 w-4 shrink-0 transition-transform group-hover/link:-translate-y-1 group-hover/link:translate-x-1 group-focus-visible/link:translate-x-1 motion-reduce:transition-none ml-1 translate-y-px"
                          />
                        </span>
                      </a>
                    </h3>
                    <p class="mt-2 text-sm leading-normal">
                      Crypto dashboard - check cryptocurrencies prices in real time.
                    </p>
                  </div>
                  <img
                    class="rounded border-2 border-slate-200/10 transition group-hover:border-slate-200/30 sm:order-1 sm:col-span-2 sm:translate-y-1 sm:max-h-18"
                    loading="lazy"
                    width="200"
                    height="48"
                    decoding="async"
                    src="@/assets/images/cryptonomicon.png"
                    alt="meetups-project-cover"
                  />
                </div>
              </li>
              <li class="mb-12">
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
                        href="https://kanban-board123.netlify.app/"
                        target="_blank"
                        rel="noreferrer"
                        aria-label="Kanban board"
                      >
                        <span
                          class="absolute -inset-x-4 -inset-y-2.5 hidden rounded md:-inset-x-6 md:-inset-y-4 lg:block"
                        ></span>
                        <span>
                          Kanban board
                          <component
                            :is="arrowUpRightIcon"
                            class="inline-block h-4 w-4 shrink-0 transition-transform group-hover/link:-translate-y-1 group-hover/link:translate-x-1 group-focus-visible/link:translate-x-1 motion-reduce:transition-none ml-1 translate-y-px"
                          />
                        </span>
                      </a>
                    </h3>
                    <p class="mt-2 text-sm leading-normal">
                      Kanban board - simple scrum board to plan sprints with your team!
                    </p>
                  </div>
                  <img
                    class="rounded border-2 border-slate-200/10 transition group-hover:border-slate-200/30 sm:order-1 sm:col-span-2 sm:translate-y-1 sm:max-h-18"
                    loading="lazy"
                    width="200"
                    height="48"
                    decoding="async"
                    src="@/assets/images/kanban-board.png"
                    alt="kanban-project-cover"
                  />
                </div>
              </li>
            </ul>
          </div>
        </section>
      </main>
    </div>
  </div>
</template>

<script>
import { defineComponent } from 'vue'
import { ArrowUpRightIcon, ArrowRightIcon } from '@heroicons/vue/24/outline'

export default defineComponent({
  name: 'AppResume',
  data () {
    return {
      activeArea: 'about'
    }
  },
  computed: {
    arrowUpRightIcon() {
      return ArrowUpRightIcon
    },
    arrowRightIcon() {
      return ArrowRightIcon
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
      const aboutSection = this.$refs.about
      const experienceSection = this.$refs.experience
      const projectsSection = this.$refs.projects
      let scrollY = window.scrollY;

      [aboutSection, experienceSection, projectsSection].forEach(current => {
        const sectionHeight = current.offsetHeight;
        const sectionTop = current.offsetTop - 50;

        if (
                scrollY > sectionTop &&
                scrollY <= sectionTop + sectionHeight
        ){
          this.activeArea = current.id
        }
      });
    }
  }
})
</script>

<style scoped lang="scss"></style>
