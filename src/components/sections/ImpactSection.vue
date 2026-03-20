<script setup>
import { ref, onMounted } from 'vue'
import gsap from 'gsap'

let counter1 = ref(0)
let counter2 = ref(0)
let counter3 = ref(0)
let counter4 = ref(0)

onMounted(() => {
  function counterTimeline() {
    let tl = gsap.timeline({ defaults: { duration: 2, ease: 'power1.out' } })

    tl.to(counter1, {
      value: 98,
      onUpdate: () => {
        counter1.value = Math.floor(counter1.value)
      },
    })
    tl.to(counter2, {
      value: 900,
      delay: -1.9,
      onUpdate: () => {
        counter2.value = Math.floor(counter2.value)
      },
    })
    tl.to(counter3, {
      value: 531,
      delay: -1.8,
      onUpdate: () => {
        counter3.value = Math.floor(counter3.value)
      },
    })
    tl.to(counter4, {
      value: 10,
      delay: -1.7,
      onUpdate: () => {
        counter4.value = Math.floor(counter4.value)
      },
    })
  }

  const mainTimeline = gsap.timeline({
    scrollTrigger: {
      trigger: '.impact-section',
      start: 'top 60%',
    },
  })

  mainTimeline.add(counterTimeline())
})
</script>

<template>
  <section class="bg-third-color impact-section">
    <div class="section-container mx-auto py-10 md:px-0">
      <div class="flex flex-col">
        <span
          class="flex flex-row items-center w-fit px-3 py-1 bg-black text-white text-small rounded-full font-semibold border border-border-color"
        >
          <div class="w-2 h-2 bg-accent-color rounded-full mr-2 animate-pulse"></div>
          Our Impact</span
        >
        <h2
          class="medium-heading font-medium text-primary-color lg:max-w-[30%] mt-10 xl:max-w-[25%] desktop:max-w-[23%]"
        >
          Numbers that speak for the <span class="text-accent-color">planet.</span>
        </h2>
        <p class="text-body text-primary-color/55 mt-3 md:max-w-[70%] lg:max-w-[50%]">
          Every program, every volunteer, and every tree we plant is living proof that collective
          action reshapes the environment one small step at a time.
        </p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-0.5 mt-10">
        <div
          class="flex flex-col gap-2 bg-fourth-color px-8 py-12 rounded-t-lg md:rounded-lg lg:rounded-l-lg lg:rounded-r-none"
        >
          <h3 class="text-display font-bold text-accent-color">{{ counter1 }}%</h3>
          <p class="text-body font-semibold text-primary-color">Customer Satisfaction</p>
          <p class="text-small text-primary-color/55 line-clamp-2">
            Volunteers who return again and again to take action with us.
          </p>
        </div>
        <div class="flex flex-col gap-2 bg-fourth-color px-8 py-12 md:rounded-lg lg:rounded-none">
          <h3 class="text-display font-bold text-accent-color">{{ counter2 }}K+</h3>
          <p class="text-body font-semibold text-primary-color">Trees Planted</p>
          <p class="text-small text-primary-color/55 line-clamp-2">
            Endemic trees thriving across forests throughout the country.
          </p>
        </div>
        <div class="flex flex-col gap-2 bg-fourth-color px-8 py-12 md:rounded-lg lg:rounded-none">
          <h3 class="text-display font-bold text-accent-color">{{ counter3 }}+</h3>
          <p class="text-body font-semibold text-primary-color">Beaches Restored</p>
          <p class="text-small text-primary-color/55 line-clamp-2">
            Coastlines freed from plastic waste and pollution damage.
          </p>
        </div>
        <div
          class="flex flex-col gap-2 bg-fourth-color px-8 py-12 rounded-b-lg md:rounded-lg lg:rounded-r-lg lg:rounded-l-none"
        >
          <h3 class="text-display font-bold text-accent-color">{{ counter4 }}+ Years</h3>
          <p class="text-body font-semibold text-primary-color">Years of Programs</p>
          <p class="text-small text-primary-color/55 line-clamp-2">
            Consistent, uninterrupted action since our founding in 2015.
          </p>
        </div>
      </div>
    </div>
  </section>
</template>
