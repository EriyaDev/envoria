<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const navbar = ref(null)

const handleScroll = () => {
  if (window.scrollY > 50) {
    navbar.value.classList.add('scrolled')
  } else {
    navbar.value.classList.remove('scrolled')
  }
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll)
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})
</script>

<template>
  <header
    ref="navbar"
    id="header"
    class="navbar bg-primary-color flex flex-row items-center justify-between w-[90%] rounded-lg p-3 transition-all duration-500"
  >
    <div class="logo"><img class="h-8" src="../assets/images/logo.svg" alt="" /></div>

    <nav>
      <ul class="flex flex-row items-center gap-10">
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

    <button class="button-primary">Contact Us</button>
  </header>
</template>
