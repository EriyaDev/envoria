<script setup>
import HeroSection from '@/components/sections/HeroSection.vue'
import ImpactSection from '@/components/sections/ImpactSection.vue'
import PurposeSection from '@/components/sections/PurposeSection.vue'
import UpcomingProgramSection from '@/components/sections/UpcomingProgramSection.vue'
import TransportationSection from '@/components/sections/TransportationSection.vue'
import BlogSection from '@/components/sections/BlogSection.vue'
import VideoSection from '@/components/sections/VideoSection.vue'
import ContactSection from '@/components/sections/ContactSection.vue'
import TestimonialSection from '@/components/sections/TestimonialSection.vue'
import CallToAction from '@/components/sections/CallToAction.vue'
import Footer from '@/components/sections/Footer.vue'

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
    :class="isVisible ? 'opacity-100 translate-y-0' : 'opacity-0'"
  >
    <HeroSection />
    <ImpactSection />
    <PurposeSection />
    <UpcomingProgramSection />
    <TransportationSection />
    <BlogSection />
    <VideoSection />
    <ContactSection />
    <TestimonialSection />
    <CallToAction />
    <Footer />
  </div>
</template>
