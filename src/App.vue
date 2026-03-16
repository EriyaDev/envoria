<script setup>
import { RouterLink, RouterView } from 'vue-router'
import Navbar from './components/Navbar.vue'
</script>

<template>
  <div class="fixed top-5 flex w-full items-center justify-center">
    <Navbar />
  </div>
  <RouterView />
</template>
