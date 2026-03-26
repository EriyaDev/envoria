<script setup>
import ButtonPrimary from '@/components/micro/ButtonPrimary.vue'
</script>

<template>
  <div class="">
    <div class="section-container py-10 lg:py-14">
      <div class="flex flex-col gap-3 items-center">
        <span
          class="flex flex-row items-center w-fit px-3 py-1 bg-black/5 text-text-text-primary-color border border-border-color/55 text-small rounded-full font-semibold"
        >
          <div class="w-2 h-2 bg-accent-color rounded-full mr-2 animate-pulse"></div>
          Need Help?</span
        >
        <h2
          class="text-display font-medium text-text-text-primary-color mt-10 text-center max-w-[90%] md:max-w-[70%] xl:max-w-[60%]"
        >
          Let’s start a <span class="text-text-primary-color/55">conversation</span>
        </h2>
      </div>
      <div class="w-full lg:max-w-[90%] mx-auto">
        <div class="bg-card-color rounded-xl p-5 lg:p-10 grid grid-cols-1 lg:grid-cols-2 gap-5">
          <div class="flex flex-col gap-2 w-full lg:col-span-2">
            <label
              for="basic-input"
              class="font-grotesk font-semibold text-text-primary-color text-sm"
              >Name<span class="text-text-primary-color/50">*</span></label
            >
            <input
              type="text"
              id="basic-input"
              class="w-full px-4 py-3 rounded-lg border border-dashed border-text-primary-color/50 focus:outline-none focus:border-accent-color transition-all font-manrope placeholder-black/30"
              placeholder="Type your full name"
            />
          </div>
          <div class="flex flex-col gap-2 w-full">
            <label
              for="basic-input"
              class="font-grotesk font-semibold text-text-primary-color text-sm"
              >Email Adress<span class="text-text-primary-color/50">*</span></label
            >
            <input
              type="email"
              id="basic-input"
              class="w-full px-4 py-3 rounded-lg border border-dashed border-text-primary-color/50 focus:outline-none focus:border-accent-color transition-all font-manrope placeholder-black/30"
              placeholder="Type your email"
            />
          </div>
          <div class="flex flex-col gap-2 w-full">
            <label
              for="basic-input"
              class="font-grotesk font-semibold text-text-primary-color text-sm"
              >Phone Number<span class="text-text-primary-color/50">*</span></label
            >
            <input
              type="tel"
              id="basic-input"
              class="w-full px-4 py-3 rounded-lg border border-dashed border-text-primary-color/50 focus:outline-none focus:border-accent-color transition-all font-manrope placeholder-black/30"
              placeholder="Type your phone number"
            />
          </div>
          <div class="flex flex-col gap-2 w-full lg:col-span-2">
            <label
              for="basic-input"
              class="font-grotesk font-semibold text-text-primary-color text-sm"
              >Name<span class="text-text-primary-color/50">*</span></label
            >
            <textarea
              type="text"
              id="basic-input"
              class="w-full px-4 py-3 rounded-lg border border-dashed border-text-primary-color/50 focus:outline-none focus:border-accent-color transition-all font-manrope placeholder-black/30"
              rows="10"
              placeholder="Type your message"
            ></textarea>
            <ButtonPrimary to="/contact"><p class="text">Submit</p></ButtonPrimary>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
