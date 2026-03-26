<script setup>
import { onMounted, ref } from 'vue'
import gsap from 'gsap'

onMounted(() => {
  let currentScroll = 0
  let isScrollingDown = true

  let tween = gsap
    .to('.marquee__part_1', { xPercent: -100, repeat: -1, duration: 20, ease: 'linear' })
    .totalProgress(0.5)

  gsap.set('.marquee__inner_1', { xPercent: -50 })

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
  <div class="flex flex-col section-container py-14">
    <div class="flex justify-center items-center">
      <h1 class="text-display">
        Trusted by <span class="text-text-primary-color/55">clients</span> and
        <span class="text-text-primary-color/55">partners</span>
      </h1>
    </div>

    <div class="w-full mx-auto mt-10">
      <section class="marquee_1 rounded-2xl relative">
        <div class="marquee__inner_1" aria-hidden="true" ref="inner">
          <div class="marquee__part_1">
            <img
              src="../../../assets/images/testimonial/brand/brand-logo-batch.svg"
              class="pr-32"
              alt=""
            />
          </div>
          <div class="marquee__part_1">
            <img
              src="../../../assets/images/testimonial/brand/brand-logo-batch.svg"
              class="pr-32"
              alt=""
            />
          </div>
          <div class="marquee__part_1">
            <img
              src="../../../assets/images/testimonial/brand/brand-logo-batch.svg"
              class="pr-32"
              alt=""
            />
          </div>
          <div class="marquee__part_1">
            <img
              src="../../../assets/images/testimonial/brand/brand-logo-batch.svg"
              class="pr-32"
              alt=""
            />
          </div>
        </div>
        <div
          class="absolute h-full top-0 left-0 w-[100px] bg-linear-to-r from-primary-color to-transparent pointer-events-none"
        ></div>
        <div
          class="absolute h-full top-0 right-0 w-[100px] bg-linear-to-l from-primary-color to-transparent pointer-events-none"
        ></div>
      </section>
    </div>
  </div>
</template>

<style scoped>
.marquee__part_1 {
  flex-shrink: 0;
  padding: 0 4px;
  font-smooth: always;
}

.marquee_1 {
  color: #eee;
  text-transform: uppercase;
  font-weight: 600;
  font-size: 1.667vw;
  padding: 32px 0;

  position: relative;
  overflow: hidden;
}

.marquee__inner_1 {
  -webkit-font-smoothing: antialiased;
  width: fit-content;
  display: flex;
  flex: auto;
  flex-direction: row;
}
</style>
