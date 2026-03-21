<script setup>
import { RouterLink, RouterView } from 'vue-router'
import Navbar from './components/Navbar.vue'
import { onMounted, onUnmounted } from 'vue'
import Lenis from 'lenis'
import gsap from 'gsap'
import ScrollTrigger from 'gsap/ScrollTrigger'

gsap.registerPlugin(ScrollTrigger)

let lenis = null

onMounted(() => {
  lenis = new Lenis({
    duration: 1.2,
    easing: (t) => Math.min(1, 1.001 - Math.pow(2, -10 * t)),
    smooth: true,
  })

  // Hook Lenis into GSAP's ticker instead of a manual RAF loop
  gsap.ticker.add((time) => {
    lenis.raf(time * 1000) // GSAP time is in seconds, Lenis expects milliseconds
  })

  // Prevent GSAP ticker lag smoothing from conflicting with Lenis
  gsap.ticker.lagSmoothing(0)

  // Keep ScrollTrigger in sync with Lenis scroll position
  lenis.on('scroll', ScrollTrigger.update)
})

onUnmounted(() => {
  if (lenis) {
    gsap.ticker.remove(lenis.raf)
    lenis.destroy()
    lenis = null
  }
})

onUnmounted(() => {
  if (rafId) cancelAnimationFrame(rafId)
  if (lenis) lenis.destroy()
})
</script>

<template>
  <div class="fixed top-5 flex w-full items-center justify-center z-50">
    <Navbar />
  </div>
  <RouterView />
</template>
