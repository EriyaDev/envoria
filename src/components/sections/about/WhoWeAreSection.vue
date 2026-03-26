<script setup>
import { ref, onMounted } from 'vue'
import gsap from 'gsap'
import { ScrollTrigger } from 'gsap/ScrollTrigger'
import { Swiper, SwiperSlide } from 'swiper/vue'
import { Navigation, Pagination, Autoplay } from 'swiper/modules'

// Import Swiper styles
import 'swiper/css'
import 'swiper/css/navigation'
import 'swiper/css/pagination'

const modules = [Navigation, Pagination, Autoplay]

const slides = ref([
  {
    id: 1,
    year: '2017',
    title: 'The Beginning',
    description:
      'Envoria was founded with a simple mission: to make waste transport smarter and more sustainable. We launched our first collection routes in two cities with a small but dedicated team.',
  },
  {
    id: 2,
    year: '2018',
    title: 'Building the Foundation',
    description:
      'Expanded our fleet and onboarded our first industrial clients. Introduced our basic route planning system and established key recycling partnerships.',
  },
  {
    id: 3,
    year: '2019',
    title: 'Going Regional',
    description:
      'Grew our network across multiple regions, serving dozens of businesses and households. Launched our first low-emission vehicle fleet dedicated to urban waste collection.',
  },
  {
    id: 1,
    year: '2020',
    title: 'Adapting and Expanding',
    description:
      'Despite global challenges, Envoria scaled operations and introduced contactless waste collection services, keeping communities clean and safe.',
  },
  {
    id: 1,
    year: '2021',
    title: 'Tech-Driven Growth',
    description:
      'Launched our real-time cargo tracking platform, giving clients full visibility of every pickup and delivery. Crossed 500+ active transport routes.',
  },
  {
    id: 1,
    year: '2022',
    title: 'Nationwide Reach',
    description:
      'Envoria expanded to cover major industrial zones nationwide. Partnered with government bodies to support large-scale environmental compliance programs.',
  },
  {
    id: 1,
    year: '2023',
    title: 'Going Global',
    description:
      'Took our first steps into international markets, establishing cross-border waste transport routes and global recycling partnerships across multiple continents.',
  },
  {
    id: 1,
    year: '2024',
    title: 'AI Integration',
    description:
      'Introduced AI-powered route optimization, cutting fuel consumption by 30% and significantly reducing our carbon footprint across all active routes.',
  },
  {
    id: 1,
    year: '2025',
    title: 'Community First Launched',
    description:
      'The Envoria household program, making sustainable waste collection accessible to families and residential communities worldwide.',
  },
  {
    id: 1,
    year: '2026',
    title: 'The Future is Green',
    description:
      'Envoria continues to grow, innovate, and lead the charge toward a zero-waste future. With 2K+ active routes and 12K+ daily collections, the journey is just beginning.',
  },
])

gsap.registerPlugin(ScrollTrigger)

let counter1 = ref(0)
let counter2 = ref(0)
let counter3 = ref(0)
let counter4 = ref(0)

onMounted(() => {
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
          <h3 class="medium-heading text-primary-color">
            Our path of continuous <span class="text-accent-color">evolution</span>
          </h3>
          <Swiper
            :slides-per-view="1"
            :loop="true"
            :space-between="0"
            :grab-cursor="true"
            :autoplay="{
              delay: 2500,
              disableOnInteraction: false,
            }"
            :navigation="{
              nextEl: '.swiper-button-next-custom',
              prevEl: '.swiper-button-prev-custom',
            }"
            :pagination="{
              el: '.swiper-pagination-custom',
              clickable: true,
            }"
            :breakpoints="{
              640: { slidesPerView: 1, spaceBetween: 0 },
            }"
            :modules="modules"
            class="overflow-hidden! w-full"
          >
            <SwiperSlide class="h-auto!" v-for="(slide, index) in slides" :key="index">
              <!-- Replace this with your actual slide content -->
              <div class="py-12">
                <div class="flex flex-col h-fit">
                  <p class="text-body text-accent-color mt-2">{{ slide.year }}</p>
                  <h4 class="small-heading text-primary-color font-medium">{{ slide.title }}</h4>
                  <p class="text-body text-primary-color font-medium mt-2">
                    {{ slide.description }}
                  </p>
                </div>
              </div>
            </SwiperSlide>
          </Swiper>
          <div class="flex flex-row items-center justify-between">
            <div class="mt-5 flex lg:max-w-[30%] flex-row justify-center gap-3">
              <div ref="prevBtn" class="swiper-button-prev-custom static! bg-[#2B2B2B]!">
                <img src="../../../assets/icons/home/prev.png" alt="" />
              </div>
              <div ref="nextBtn" class="swiper-button-next-custom static! bg-[#2B2B2B]!">
                <img src="../../../assets/icons/home/next.png" alt="" />
              </div>
            </div>
            <div
              class="swiper-pagination-custom mt-5 flex flex-row gap-1.5 md:gap-2 items-center justify-end static!"
            ></div>
          </div>
        </div>
        <div class="w-full h-80 lg:h-full rounded-xl overflow-hidden">
          <img
            class="w-full h-full object-cover object-left"
            src="../../../assets/images/who-we-are/journey.webp"
            alt=""
          />
        </div>
      </div>
    </div>
  </div>
</template>
