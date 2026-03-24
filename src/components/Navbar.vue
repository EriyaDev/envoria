<script setup>
import { ref, onMounted, onUnmounted } from 'vue'
import ButtonPrimary from './micro/ButtonPrimary.vue'

const navbar = ref(null)
const mobileNabvar = ref(null)

const handleScroll = () => {
  if (window.scrollY > 50) {
    navbar.value.classList.add('scrolled')
  } else {
    navbar.value.classList.remove('scrolled')
  }
}

const handleNavbar = () => {
  mobileNabvar.value.classList.toggle('!h-[240px]')
}

onMounted(() => {
  if (window.innerWidth >= 1024) {
    window.addEventListener('scroll', handleScroll)
  } // Disable scroll effect on mobile
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})
</script>

<template>
  <header
    ref="navbar"
    id="header"
    class="navbar z-50 bg-primary-color flex flex-row items-center justify-between w-[85%] rounded-lg p-3 transition-all ease-out duration-500"
  >
    <div class="logo"><img class="h-7" src="../assets/images/logo.svg" alt="" /></div>

    <nav>
      <ul class="hidden lg:flex flex-row items-center gap-10">
        <li class="relative group">
          <router-link class="nav-link" to="/">Home</router-link>
          <div class="nav-link-underline"></div>
        </li>
        <li class="relative group">
          <router-link class="nav-link" to="/about">About Us</router-link>
          <div class="nav-link-underline"></div>
        </li>
        <li class="relative group">
          <router-link class="nav-link" to="/program">Program</router-link>
          <div class="nav-link-underline"></div>
        </li>
        <li class="relative group">
          <router-link class="nav-link" to="/blog">Blog</router-link>
          <div class="nav-link-underline"></div>
        </li>
      </ul>
    </nav>

    <nav
      id="nav-mobile"
      ref="mobileNabvar"
      class="absolute top-11 left-0 right-0 overflow-hidden h-0 transition-all duration-700 ease-out"
    >
      <ul class="flex flex-col gap-5 bg-primary-color rounded-b-lg p-10 w-[85%] mx-auto z-40">
        <li class="relative w-fit group">
          <router-link class="nav-link" to="/">Home</router-link>
          <div class="nav-link-underline"></div>
        </li>
        <li class="relative w-fit group">
          <router-link class="nav-link" to="/about">About Us</router-link>
          <div class="nav-link-underline"></div>
        </li>
        <li class="relative w-fit group">
          <router-link class="nav-link" to="/program">Program</router-link>
          <div class="nav-link-underline"></div>
        </li>
        <li class="relative w-fit group">
          <router-link class="nav-link" to="/blog">Blog</router-link>
          <div class="nav-link-underline"></div>
        </li>
      </ul>
    </nav>

    <div class="flex flex-row items-center gap-5">
      <button v-on:click="handleNavbar" class="last:hidden">
        <i class="ri-menu-3-line text-2xl"></i>
      </button>
      <div class="hidden lg:flex">
        <ButtonPrimary to="/contact">Contact Us</ButtonPrimary>
      </div>
    </div>
  </header>
</template>
