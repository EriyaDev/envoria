<script setup>
import { onMounted, ref } from 'vue'
import gsap from 'gsap'
import { Swiper, SwiperSlide } from 'swiper/vue'
import { Navigation, Pagination, Autoplay } from 'swiper/modules'

// Import Swiper styles
import 'swiper/css'
import 'swiper/css/navigation'
import 'swiper/css/pagination'

const modules = [Navigation, Pagination, Autoplay]

// Replace with your actual slide data
const slides = ref([
  {
    id: 1,
    image_path: new URL('../../assets/images/testimonial/profile.svg', import.meta.url).href,
    name: 'Daiga Ellaby',
    place: 'Las Vegas, United States',
    message:
      'We were struggling to manage our factory waste until we found Envoria. The collection was seamless, on schedule, and the team was incredibly professional.',
  },
  {
    id: 2,
    image_path: new URL('../../assets/images/testimonial/profile-2.svg', import.meta.url).href,
    name: 'Franz Hermánn',
    place: 'Nurbürg, Germany',
    message:
      'Envoria transformed how we handle waste at our facility. Real-time tracking gave us full visibility and the routes were always optimized. Highly recommend.',
  },
  {
    id: 3,
    image_path: new URL('../../assets/images/testimonial/profile-3.svg', import.meta.url).href,
    name: 'Charles Leclerc',
    place: 'Monte Carlo, Monaco',
    message:
      'Switching to Envoria was the best decision for our business. Our waste disposal costs dropped significantly and the whole process became stress-free.',
  },
  {
    id: 4,
    image_path: new URL('../../assets/images/testimonial/profile.svg', import.meta.url).href,
    name: 'Ryan’s Family',
    place: 'Orchard, Singapore',
    message:
      'As a household, we never thought waste management could be this easy. Envoria picked up everything on time, sorted it responsibly, and even sent us a recycling summary.',
  },
  {
    id: 5,
    image_path: new URL('../../assets/images/testimonial/profile-1.svg', import.meta.url).href,
    name: 'Aiony Haust',
    place: 'Orchard, Singapore',
    message:
      'We operate across multiple sites and Envoria manages all of them without missing a beat. One platform, one team, zero headaches.',
  },
  {
    id: 6,
    image_path: new URL('../../assets/images/testimonial/profile.svg', import.meta.url).href,
    name: 'Daiga Ellaby',
    place: 'Las Vegas, United States',
    message:
      'We were struggling to manage our factory waste until we found Envoria. The collection was seamless, on schedule, and the team was incredibly professional.',
  },
  {
    id: 7,
    image_path: new URL('../../assets/images/testimonial/profile-2.svg', import.meta.url).href,
    name: 'Franz Hermánn',
    place: 'Nurbürg, Germany',
    message:
      'Envoria transformed how we handle waste at our facility. Real-time tracking gave us full visibility and the routes were always optimized. Highly recommend.',
  },
  {
    id: 8,
    image_path: new URL('../../assets/images/testimonial/profile-3.svg', import.meta.url).href,
    name: 'Charles Leclerc',
    place: 'Monte Carlo, Monaco',
    message:
      'Switching to Envoria was the best decision for our business. Our waste disposal costs dropped significantly and the whole process became stress-free.',
  },
  {
    id: 9,
    image_path: new URL('../../assets/images/testimonial/profile.svg', import.meta.url).href,
    name: 'Ryan’s Family',
    place: 'Orchard, Singapore',
    message:
      'As a household, we never thought waste management could be this easy. Envoria picked up everything on time, sorted it responsibly, and even sent us a recycling summary.',
  },
  {
    id: 10,
    image_path: new URL('../../assets/images/testimonial/profile-1.svg', import.meta.url).href,
    name: 'Aiony Haust',
    place: 'Orchard, Singapore',
    message:
      'We operate across multiple sites and Envoria manages all of them without missing a beat. One platform, one team, zero headaches.',
  },
])

let xPercent = 0

onMounted(() => {
  let currentScroll = 0
  let isScrollingDown = true

  let tween = gsap
    .to('.marquee__part', { xPercent: -100, repeat: -1, duration: 20, ease: 'linear' })
    .totalProgress(0.5)

  gsap.set('.marquee__inner', { xPercent: -50 })

  window.addEventListener('scroll', function () {
    if (window.pageYOffset > currentScroll) {
      isScrollingDown = true
    } else {
      isScrollingDown = false
    }

    gsap.to(tween, {
      timeScale: isScrollingDown ? 1 : -1,
    })

    currentScroll = window.pageYOffset
  })
})
</script>

<template>
  <div class="py-10 md:px-0">
    <!-- <div class="flex flex-col gap-5 lg:flex-row items-center lg:justify-between">
      <div class="flex flex-col gap-3 items-start">
        <span
          class="flex flex-row items-center w-fit px-3 py-1 bg-black/5 text-text-primary-color border border-[#2D612B]/13 text-small rounded-full font-semibold animate-pulse"
        >
          <div class="w-2 h-2 bg-accent-color rounded-full mr-2"></div>
          Trusted by customers
        </span>

        <div class="flex flex-col gap-4">
          <h2 class="medium-heading font-medium text-text-primary-color mt-10 text-start">
            What people say <br />about <span class="text-text-primary-color/55">Envoria</span>
          </h2>
          <p class="text-body font-medium xl:max-w-[70%] text-[#464646]">
            We strive to make our waste transport process simple and accessible to every business.
          </p>
        </div>
      </div>
    </div> -->

    <div class="testimonial-section">
      <div
        class="section-container mx-auto flex flex-col lg:flex-row lg:items-end lg:justify-between gap-3"
      >
        <div
          class="flex w-full flex-row items-end justify-between gap-5"
          data-aos="fade-up"
          data-aos-duration="1000"
        >
          <div class="flex flex-col gap-3 items-start">
            <span
              class="flex flex-row items-center w-fit px-3 py-1 bg-black/5 text-text-primary-color border border-[#2D612B]/13 text-small rounded-full font-semibold"
            >
              <div class="w-2 h-2 bg-accent-color rounded-full mr-2 animate-pulse"></div>
              Trusted by customers
            </span>
            <div class="flex flex-col gap-4">
              <h2 class="medium-heading font-medium text-text-primary-color mt-10 text-start">
                What people say <br />about <span class="text-text-primary-color/55">Envoria</span>
              </h2>
              <p class="text-body font-medium xl:max-w-[70%] text-[#464646]">
                We strive to make our waste transport process simple and accessible to every
                business.
              </p>
            </div>
          </div>
        </div>

        <div class="flex w-full justify-end">
          <div class="mt-5 flex lg:max-w-[30%] flex-row justify-center gap-3">
            <div
              ref="prevBtn"
              class="swiper-button-prev-custom"
              style="position: static !important"
            >
              <img src="../../assets/icons/home/prev.png" alt="" />
            </div>
            <div
              ref="nextBtn"
              class="swiper-button-next-custom"
              style="position: static !important"
            >
              <img src="../../assets/icons/home/next.png" alt="" />
            </div>
          </div>
        </div>
      </div>

      <Swiper
        :slides-per-view="1.2"
        :loop="true"
        :centeredSlides="true"
        :space-between="30"
        :grab-cursor="true"
        :pagination="false"
        :initial-slide="2"
        :autoplay="{
          delay: 2500,
          disableOnInteraction: false,
        }"
        :navigation="{
          nextEl: '.swiper-button-next-custom',
          prevEl: '.swiper-button-prev-custom',
        }"
        :breakpoints="{
          640: { slidesPerView: 1.5, spaceBetween: 25 },
          768: { slidesPerView: 2.1, spaceBetween: 25 },
          1024: { slidesPerView: 3.2, spaceBetween: 25 },
          1440: { slidesPerView: 4, spaceBetween: 25 },
        }"
        :modules="modules"
        class="swiper-wrapper mt-10"
      >
        <SwiperSlide v-for="(slide, index) in slides" :key="index">
          <div data-aos="fade-up" data-aos-duration="1000" data-aos-delay="0" class="h-full w-full">
            <!-- Replace this with your actual slide content -->
            <div class="bg-card-color p-10 rounded-2xl h-96 lg:h-96">
              <div class="flex flex-col justify-between h-full">
                <p class="text-body">
                  {{ slide.message }}
                </p>

                <div
                  class="flex flex-row gap-4 items-center pt-6 border-t border-t-border-color border-dashed"
                >
                  <img :src="slide.image_path" :alt="slide.name" />
                  <div class="flex flex-col">
                    <h4 class="small-heading font-medium">{{ slide.name }}</h4>
                    <p class="text-body text-text-primary-color/55">{{ slide.place }}</p>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </SwiperSlide>
      </Swiper>

      <div class="w-[85%] mx-auto mt-10">
        <section class="marquee bg-card-color rounded-2xl relative">
          <div class="marquee__inner" aria-hidden="true" ref="inner">
            <div class="marquee__part">
              <img
                src="../../assets/images/testimonial/brand/brand-logo-batch.svg"
                class="pr-32"
                alt=""
              />
            </div>
            <div class="marquee__part">
              <img
                src="../../assets/images/testimonial/brand/brand-logo-batch.svg"
                class="pr-32"
                alt=""
              />
            </div>
            <div class="marquee__part">
              <img
                src="../../assets/images/testimonial/brand/brand-logo-batch.svg"
                class="pr-32"
                alt=""
              />
            </div>
            <div class="marquee__part">
              <img
                src="../../assets/images/testimonial/brand/brand-logo-batch.svg"
                class="pr-32"
                alt=""
              />
            </div>
          </div>
          <div
            class="absolute h-full top-0 left-0 w-[100px] bg-linear-to-r from-card-color to-transparent pointer-events-none"
          ></div>
          <div
            class="absolute h-full top-0 right-0 w-[100px] bg-linear-to-l from-card-color to-transparent pointer-events-none"
          ></div>
        </section>
      </div>
    </div>
  </div>
</template>

<style scoped>
.marquee__part {
  flex-shrink: 0;
  padding: 0 4px;
  font-smooth: always;
}

.marquee {
  color: #eee;
  text-transform: uppercase;
  font-weight: 600;
  font-size: 1.667vw;
  padding: 32px 0;

  position: relative;
  overflow: hidden;
}

.marquee__inner {
  -webkit-font-smoothing: antialiased;
  width: fit-content;
  display: flex;
  flex: auto;
  flex-direction: row;
}
</style>
