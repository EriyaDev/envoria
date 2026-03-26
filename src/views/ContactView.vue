<script setup>
import FaqSection from '@/components/sections/about/FaqSection.vue'
import WhereWeOperate from '@/components/sections/about/WhereWeOperate.vue'
import ContactForm from '@/components/sections/contact/ContactForm.vue'
import ContactHeroSection from '@/components/sections/contact/ContactHeroSection.vue'
import ContactUs from '@/components/sections/contact/ContactUs.vue'
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
    <ContactHeroSection />
    <ContactUs />
    <ContactForm />
    <WhereWeOperate />
    <FaqSection />
    <Footer />
  </div>
</template>
