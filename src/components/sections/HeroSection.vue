<script setup>
import ButtonPrimary from '../micro/ButtonPrimary.vue'
import { ref, onMounted, onUnmounted } from 'vue'
import Typed from 'typed.js'
import gsap from 'gsap'

const typedEl = ref(null)
let typed = null

onMounted(() => {
  typed = new Typed(typedEl.value, {
    strings: ['cleaner world', 'better environment', 'healthier earth'],
    typeSpeed: 60,
    backSpeed: 40,
    loop: true,
    // showCursor: false,
  })
})

// onMounted(() => {
//   const leftCol = document.querySelector('.hero-col-left')
//   const rightCol = document.querySelector('.hero-col-right')

//   const totalHeight = leftCol.scrollHeight / 2 // separuh = 1 set asli

//   // LEFT — scroll ke atas
//   gsap.to(leftCol, {
//     y: -totalHeight,
//     duration: 8,
//     ease: 'none',
//     repeat: -1,
//     modifiers: {
//       y: gsap.utils.unitize((y) => parseFloat(y) % totalHeight),
//     },
//   })

//   // RIGHT — scroll ke bawah
//   gsap.fromTo(
//     rightCol,
//     { y: -totalHeight },
//     {
//       y: 0,
//       duration: 8,
//       ease: 'none',
//       repeat: -1,
//       modifiers: {
//         y: gsap.utils.unitize((y) => {
//           const val = parseFloat(y) % totalHeight
//           return val > 0 ? val - totalHeight : val
//         }),
//       },
//     },
//   )
// })

onUnmounted(() => {
  typed.destroy()
})
</script>

<template>
  <section class="min-h-screen bg-secondary-color">
    <div class="grid grid-cols-5 lg:grid-cols-10 section-container gap-10 px-3 md:px-0">
      <!-- LEFT: Text -->
      <div
        class="flex flex-col justify-center text-left py-16 h-screen w-full col-span-5 lg:col-span-10 xl:col-span-5"
      >
        <h1 class="text-display font-semibold mb-6">
          Innovation rooted in nature for a <span ref="typedEl"></span>
        </h1>
        <p class="text-body text-gray-500 leading-relaxed mb-8 md:max-w-[70%]">
          Join a community of eco-enthusiasts taking meaningful actions to protect nature and create
          a greener future.
        </p>
        <div class="flex flex-row items-center gap-3 md:gap-5">
          <button
            class="bg-black flex items-center gap-1 text-white font-family-inter text-base py-3 px-6 rounded-full hover:bg-black/75 transition-colors duration-300 hover:cursor-pointer"
          >
            <img src="../../assets/icons/home/leaf.svg" alt="" />
            <p class="text-body font-medium">Join Action</p>
          </button>
          <ButtonPrimary to="/about">
            <img src="../../assets/icons/home/heart.svg" alt="" />
            <p class="text-body">Donate Now</p></ButtonPrimary
          >
        </div>
      </div>

      <!-- RIGHT: Image -->
      <div
        class="lg:h-screen hidden xl:flex items-center justify-center w-full col-span-5 lg:col-span-3 xl:col-span-5"
      >
        <div class="relative w-full h-full flex flex-row lg:gap-4 xl:gap-6 overflow-hidden z-0">
          <!-- LEFT IMAGE COLLECTION -->
          <div class="hero-col flex flex-col whitespace-nowrap top-0" id="left-col">
            <img src="../../assets/images/hero/lt.webp" alt="" />
            <img src="../../assets/images/hero/lm.webp" alt="" />
            <img src="../../assets/images/hero/lb.webp" alt="" />
            <!-- clone 1 -->
            <img src="../../assets/images/hero/lt.webp" alt="" />
            <img src="../../assets/images/hero/lm.webp" alt="" />
            <img src="../../assets/images/hero/lb.webp" alt="" />
          </div>
          <!-- RIGHT IMAGE COLLECTION -->
          <div class="hero-col flex flex-col whitespace-nowrap top-0" id="right-col">
            <img src="../../assets/images/hero/rt.webp" alt="" />
            <img src="../../assets/images/hero/rm.webp" alt="" />
            <img src="../../assets/images/hero/rb.webp" alt="" />
            <!-- clone 1 -->
            <img src="../../assets/images/hero/rt.webp" alt="" />
            <img src="../../assets/images/hero/rm.webp" alt="" />
            <img src="../../assets/images/hero/rb.webp" alt="" />
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style></style>
