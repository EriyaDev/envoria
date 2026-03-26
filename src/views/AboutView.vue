<script setup>
import AboutSection from '@/components/sections/about/AboutSection.vue'
import FaqSection from '@/components/sections/about/FaqSection.vue'
import TrustedBySection from '@/components/sections/about/TrustedBySection.vue'
import WhereWeOperate from '@/components/sections/about/WhereWeOperate.vue'
import WhoWeAreSection from '@/components/sections/about/WhoWeAreSection.vue'
import BlogSection from '@/components/sections/BlogSection.vue'
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
    :class="isVisible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-6'"
  >
    <AboutSection />
    <WhoWeAreSection />
    <WhereWeOperate />
    <TrustedBySection />
    <FaqSection />
    <BlogSection />
    <CallToAction />
    <Footer />
  </div>
</template>
