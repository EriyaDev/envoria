<script setup>
import ButtonPrimary from '../micro/ButtonPrimary.vue'
</script>

<template>
  <div class="relative w-full h-96 md:h-80 lg:h-full">
    <img
      src="../../assets/images/call-to-action/cta.png"
      alt="call to action"
      class="w-full h-full object-cover"
    />

    <div class="absolute inset-0 flex flex-col items-center justify-center gap-12">
      <span
        class="flex flex-row items-center w-fit px-3 py-1 bg-primary-color text-text-primary-color border text-small rounded-full"
      >
        <p class="text-body capitalize">Start your journey</p>
      </span>
      <h1 class="text-display text-primary-color text-center font-semibold lg:max-w-[40%]">
        Join the mission for smarter, cleaner waste movement
      </h1>
      <ButtonPrimary to="/about">
        <img src="../../assets/icons/home/leaf-black.svg" alt="" />
        <p class="text-body">Safe Our Planet</p></ButtonPrimary
      >
    </div>
  </div>
</template>
