<script setup>
import { onMounted, ref } from 'vue'
import gsap from 'gsap'
let xPercent = 0

onMounted(() => {
  let currentScroll = 0
  let isScrollingDown = true

  let tween = gsap
    .to('.marquee__part', { xPercent: -100, repeat: -1, duration: 50, ease: 'linear' })
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
  <div class="bg-card-color pt-32">
    <section class="section-container">
      <div class="flex flex-col gap-3 items-start">
        <span
          class="flex flex-row items-center w-fit px-3 py-1 bg-black/5 text-text-primary-color border border-[#2D612B]/13 text-small rounded-full font-semibold"
        >
          <div class="w-2 h-2 bg-accent-color rounded-full mr-2 animate-pulse"></div>
          About Us
        </span>
        <h2 class="text-display font-medium text-text-primary-color mt-5 text-start">
          Where <span class="text-text-primary-color/55">purpose</span> meets <br />
          <span class="text-text-primary-color/55">efficiency</span> in every waste move
        </h2>
      </div>
    </section>
    <section class="marquee rounded-2xl relative">
      <div class="marquee__inner" aria-hidden="true" ref="inner">
        <div class="marquee__part">
          <img src="../../../assets/images/about/about-marquee.webp" class="pr-2 h-96" alt="" />
        </div>
        <div class="marquee__part">
          <img src="../../../assets/images/about/about-marquee.webp" class="pr-2 h-96" alt="" />
        </div>
        <div class="marquee__part">
          <img src="../../../assets/images/about/about-marquee.webp" class="pr-2 h-96" alt="" />
        </div>
      </div>
    </section>
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
