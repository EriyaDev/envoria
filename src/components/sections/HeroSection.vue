<script setup>
import ButtonPrimary from '../micro/ButtonPrimary.vue'
</script>

<template>
  <section class="flex flex-col md:flex-row min-h-screen bg-secondary-color">
    <!-- LEFT: Text -->
    <div class="flex flex-col justify-center text-left px-10 py-16 md:px-16 md:w-1/2">
      <h1 class="text-display font-semibold mb-6">
        Innovation rooted in nature for a cleaner world
      </h1>
      <p class="text-body text-gray-500 leading-relaxed mb-8 max-w-[70%]">
        Join a community of eco-enthusiasts taking meaningful actions to protect nature and create a
        greener future.
      </p>
      <div class="flex flex-row items-center gap-5">
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
    <div class="md:w-1/2 h-64 md:h-auto">
      <img
        src="../../assets/images/hero/hero.webp"
        alt="Hero image"
        class="w-full h-full object-cover"
        style="height: 100vh"
      />
    </div>
  </section>
</template>
