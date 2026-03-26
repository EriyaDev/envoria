<script setup>
import { ref, onMounted } from 'vue'
import gsap from 'gsap'
import { ScrollTrigger } from 'gsap/ScrollTrigger'

gsap.registerPlugin(ScrollTrigger)

let counter1 = ref(0)
let counter2 = ref(0)
let counter3 = ref(0)
let counter4 = ref(0)

onMounted(() => {
  // function counterTimeline() {
  // let tl = gsap.timeline({ defaults: { duration: 2, ease: 'power1.out' } })

  gsap.to(counter1, {
    value: 98,
    duration: 2,
    scrollTrigger: {
      trigger: '.impact-section',
      start: 'top 60%',
    },
    onUpdate: () => {
      counter1.value = Math.floor(counter1.value)
    },
  })
  gsap.to(counter2, {
    value: 900,
    duration: 2,
    scrollTrigger: {
      trigger: '.impact-section',
      start: 'top 60%',
    },
    onUpdate: () => {
      counter2.value = Math.floor(counter2.value)
    },
  })
  gsap.to(counter3, {
    value: 531,
    duration: 2,
    scrollTrigger: {
      trigger: '.impact-section',
      start: 'top 60%',
    },
    onUpdate: () => {
      counter3.value = Math.floor(counter3.value)
    },
  })
  gsap.to(counter4, {
    value: 10,
    duration: 2,
    scrollTrigger: {
      trigger: '.impact-section',
      start: 'top 60%',
    },
    onUpdate: () => {
      counter4.value = Math.floor(counter4.value)
    },
  })
  // }

  // const mainTimeline = gsap.timeline({
  //   scrollTrigger: {
  //     trigger: '.impact-section',
  //     start: 'top 60%',
  //   },
  // })

  // mainTimeline.add(counterTimeline())
  // mainTimeline.play()
})
</script>

<template>
  <div class="section-container py-14">
    <div class="grid grid-cols-1 gap-10">
      <div class="flex flex-col gap-3 items-center">
        <span
          class="flex flex-row items-center w-fit px-3 py-1 bg-black/5 text-text-text-primary-color border border-border-color/55 text-small rounded-full font-semibold"
        >
          <div class="w-2 h-2 bg-accent-color rounded-full mr-2 animate-pulse"></div>
          Who we are</span
        >
        <h2
          class="text-display font-medium text-text-text-primary-color mt-10 text-center max-w-[90%] md:max-w-[70%] xl:max-w-[60%]"
        >
          Smart waste transport solutions for a
          <span class="text-text-text-primary-color/55">cleaner, greener world</span>
        </h2>
        <p class="text-body lg:max-w-[60%] text-center opacity-75">
          At Envoria, we believe waste movement should be as kind to the planet as it is efficient
          for business. Born from a vision to create smarter, sustainable waste logistics, we set
          out to challenge the way waste is collected, transported, and recycled.
        </p>
      </div>
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-1">
        <div
          class="relative group flex overflow-hidden flex-col gap-2 bg-card-color px-8 py-12 rounded-t-lg md:rounded-lg lg:rounded-l-lg lg:rounded-r-none"
        >
          <h3 class="text-display font-bold text-text-text-primary-color">{{ counter1 }}%</h3>
          <p class="text-body font-semibold text-text-primary-color">Customer Satisfaction</p>
          <p class="text-small text-text-primary-color/55 line-clamp-2">
            Volunteers who return again and again to take action with us.
          </p>
        </div>
        <div
          class="relative group flex overflow-hidden flex-col gap-2 bg-card-color px-8 py-12 md:rounded-lg lg:rounded-none"
        >
          <h3 class="text-display font-bold text-text-text-primary-color">
            {{ counter4 }}M+ People
          </h3>
          <p class="text-body font-semibold text-text-primary-color">Satisfied customers</p>
          <p class="text-small text-text-primary-color/55 line-clamp-2">
            Endemic trees thriving across forests throughout the country.
          </p>
        </div>
        <div
          class="relative group flex overflow-hidden flex-col gap-2 bg-card-color px-8 py-12 rounded-b-lg md:rounded-lg lg:rounded-r-lg lg:rounded-l-none"
        >
          <h3 class="text-display font-bold text-text-text-primary-color">{{ counter4 }}+ Years</h3>
          <p class="text-body font-semibold text-text-primary-color">Years of Programs</p>
          <p class="text-small text-text-primary-color/55 line-clamp-2">
            Consistent, uninterrupted action since our founding in 2015.
          </p>
        </div>
      </div>
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-20">
        <div class="w-full h-72 lg:h-full rounded-lg">
          <img src="../../../assets/images/who-we-are/who-we-are.webp" alt="" />
        </div>
        <div class="flex flex-col">
          <h2 class="text-display">
            Why choose <span class="text-text-primary-color/55">us?</span>
          </h2>
          <p class="text-body opacity-75 mt-3">
            We deliver speed, reliability, and sustainability, putting our clients and the planet
            first every step of the way.
          </p>
          <ul class="mt-5 lg:mt-10 flex flex-col gap-3 lg:gap-5">
            <li class="flex items-center gap-2">
              <img src="../../../assets/icons/home/checkmark-green.svg" alt="" />
              <span class="text-body font-medium text-text-primary-color/75"
                >Fast waste collection & dispatch</span
              >
            </li>
            <li class="flex items-center gap-2">
              <img src="../../../assets/icons/home/checkmark-green.svg" alt="" />
              <span class="text-body font-medium text-text-primary-color/75"
                >Transparent route tracking</span
              >
            </li>
            <li class="flex items-center gap-2">
              <img src="../../../assets/icons/home/checkmark-green.svg" alt="" />
              <span class="text-body font-medium text-text-primary-color/75"
                >Eco-friendly commitment</span
              >
            </li>
          </ul>
        </div>
      </div>

      <div class="grid grid-cols-1 lg:grid-cols-2 gap-7">
        <div class="bg-third-color rounded-xl p-5 lg:p-10">
          <h3 class="medium-heading">Our path of continuous evolution</h3>
        </div>
      </div>
    </div>
  </div>
</template>
