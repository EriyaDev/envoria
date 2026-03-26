<script setup>
import RecentBlogSection from '@/components/sections/RecentBlogSection.vue'
import CallToActionSection from '@/components/sections/CallToAction.vue'
import Footer from '@/components/sections/Footer.vue'
import BlogDetailSection from '@/components/sections/BlogDetailSection.vue'
import BlogSection from '@/components/sections/BlogSection.vue'
import BlogReusableSection from '@/components/sections/BlogReusableSection.vue'
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
    <BlogDetailSection />
    <BlogReusableSection />
    <CallToActionSection />
    <Footer />
  </div>
</template>
