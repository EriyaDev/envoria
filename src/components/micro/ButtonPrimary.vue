<script setup>
const props = defineProps({
  to: {
    type: String,
    required: true,
  },
})
</script>

<template>
  <router-link :to="props.to" class="button-primary">
    <slot></slot>
  </router-link>
</template>
