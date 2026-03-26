<script setup>
import { ref, onMounted } from 'vue'
import gsap from 'gsap'
import { ScrollTrigger } from 'gsap/ScrollTrigger'

gsap.registerPlugin(ScrollTrigger)
</script>

<template>
  <section class="bg-third-color impact-section">
    <div class="section-container mx-auto py-10 md:px-0">
      <div class="flex flex-col items-center text-center">
        <span
          class="flex flex-row items-center w-fit px-3 py-1 bg-black text-white text-small rounded-full font-semibold border border-border-color"
        >
          <div class="w-2 h-2 bg-accent-color rounded-full mr-2 animate-pulse"></div>
          Contact Us</span
        >
        <h2
          data-aos="fade-up"
          data-aos-delay="00"
          class="text-display font-medium text-primary-color lg:max-w-[30%] mt-10 xl:max-w-[40%] desktop:max-w-[23%]"
        >
          Envoria is <span class="text-accent-color">always</span> on standby
        </h2>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-0.5 mt-10">
        <div
          data-aos="fade-up"
          data-aos-delay="00"
          class="relative group flex overflow-hidden flex-col gap-2 bg-fourth-color px-8 py-12 rounded-t-lg md:rounded-lg lg:rounded-l-lg lg:rounded-r-none"
        >
          <h3
            class="text-display font-bold text-accent-color overflow-auto text-nowrap scroll-hidden"
          >
            Call us anytime
          </h3>
          <p class="text-small text-primary-color line-clamp-2 mt-3">+123-456-7890</p>
          <p class="text-small text-primary-color line-clamp-2">+ 987-654-3210</p>
          <div
            class="absolute bottom-0 left-0 h-1 bg-accent-color w-0 group-hover:w-full transition-all duration-300"
          ></div>
        </div>
        <div
          data-aos="fade-up"
          data-aos-delay="200"
          class="relative group flex overflow-hidden flex-col gap-2 bg-fourth-color px-8 py-12 md:rounded-lg lg:rounded-none"
        >
          <h3 class="text-display font-bold text-accent-color">Write to us</h3>
          <p class="text-small text-primary-color line-clamp-2 mt-3">hello@example.com</p>
          <p class="text-small text-primary-color line-clamp-2">hello@envoria.com</p>
          <div
            class="absolute bottom-0 left-0 h-1 bg-accent-color w-0 group-hover:w-full transition-all duration-300"
          ></div>
        </div>
        <div
          data-aos="fade-up"
          data-aos-delay="400"
          class="relative group flex overflow-hidden flex-col gap-2 bg-fourth-color px-8 py-12 rounded-b-lg md:rounded-lg lg:rounded-r-lg lg:rounded-l-none"
        >
          <h3 class="text-display font-bold text-accent-color">Open hours</h3>
          <p class="text-small text-primary-color line-clamp-2 mt-3">
            Mon-Sat: 08:00 AM – 10:00 PM
          </p>
          <p class="text-small text-primary-color line-clamp-2">Sun: Out for a breather</p>
          <div
            class="absolute bottom-0 left-0 h-1 bg-accent-color w-0 group-hover:w-full transition-all duration-300"
          ></div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scope>
.scroll-hidden::-webkit-scrollbar {
  display: none;
  width: 0;
}
</style>
