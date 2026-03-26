<script setup>
import ProgramHeroSection from '@/components/sections/ProgramHeroSection.vue'
import ProgramHighlightSection from '@/components/sections/ProgramHighlightSection.vue'
import ProgramActionSection from '@/components/sections/ProgramActionSection.vue'
import BlogReusableSection from '@/components/sections/BlogReusableSection.vue'
import CallToActionSection from '@/components/sections/CallToAction.vue'
import Footer from '@/components/sections/Footer.vue'
import ProgramCrowdfundingSection from '@/components/sections/ProgramCrowdfundingSection.vue'
import ProgramWorkshopSection from '@/components/sections/ProgramWorkshopSection.vue'

import { ref, onMounted } from 'vue'

const isVisible = ref(false)

onMounted(() => {
  requestAnimationFrame(() => {
    isVisible.value = true
  })
})
</script>

<template>
  <div
    class="transition-all duration-300"
    :class="isVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-6'"
  >
    <ProgramHeroSection />
    <ProgramHighlightSection />
    <ProgramActionSection />
    <ProgramCrowdfundingSection />
    <ProgramWorkshopSection />
    <BlogReusableSection />
    <CallToActionSection />
    <Footer />
  </div>
</template>
