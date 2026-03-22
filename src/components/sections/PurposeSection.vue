<script setup>
import ButtonPrimary from '../micro/ButtonPrimary.vue'
</script>

<template>
  <div class="section-container mx-auto py-10">
    <div class="flex flex-col gap-3 items-center">
      <span
        class="flex flex-row items-center w-fit px-3 py-1 bg-black/5 text-text-primary-color border border-border-color/55 text-small rounded-full font-semibold"
      >
        <div class="w-2 h-2 bg-accent-color rounded-full mr-2"></div>
        Our Purpose</span
      >
      <h2
        class="medium-heading font-medium text-text-primary-color mt-10 text-center max-w-[90%] md:max-w-[70%] xl:max-w-[37%]"
      >
        Envoria is building the bridge between
        <span class="text-text-primary-color/55">passionate people</span> and the planet that
        <span class="text-text-primary-color/55">needs them most</span>.
      </h2>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 mt-10">
      <div class="flex flex-col bg-fourth-color rounded-2xl px-7 py-10 justify-between">
        <div class="flex flex-col">
          <h4 class="small-heading uppercase text-primary-color">WE HELP OVER</h4>
          <h3 class="text-display font-bold text-accent-color mt-7">3.1Million+</h3>
        </div>
        <p class="text-body text-primary-color line-clamp-5 mt-3">
          Helping communities around the world gain access to sustainable resources, environmental
          programs, and initiatives that improve quality of life while protecting the planet.
        </p>
      </div>
      <div class="relative bg-fourth-color rounded-2xl">
        <img src="../../assets/images/purpose/card.webp" alt="" class="w-full h-full rounded-2xl" />
        <div class="absolute bottom-10 w-full px-5">
          <h4 class="small-heading font-semibold uppercase text-primary-color">VISION</h4>
          <p class="text-body text-primary-color line-clamp-5 mt-2">
            Helping communities around the world gain access to sustainable resources, environmental
            programs, and initiatives that improve quality of life while protecting the planet.
          </p>
        </div>
      </div>
      <div
        class="flex flex-col bg-fourth-color rounded-2xl px-7 py-10 justify-between md:col-span-2 lg:col-span-1"
      >
        <div class="flex flex-col">
          <h4 class="small-heading uppercase text-primary-color">OUR MISSION</h4>
          <h3 class="medium-heading font-bold text-accent-color uppercase">
            Moving logistics toward sustainability.
          </h3>
        </div>
        <p class="text-body text-primary-color line-clamp-5 mt-3">
          Every cleanup, every tree, every educated mind is a step closer to the world we're
          building. We connect action to impact at every level.
        </p>
      </div>
    </div>

    <div class="flex w-full justify-center items-center mt-5">
      <ButtonPrimary to="/about">
        <img src="../../assets/icons/home/leaf-black.svg" alt="" />
        <p class="text-body">More About Us</p></ButtonPrimary
      >
    </div>
  </div>
</template>
