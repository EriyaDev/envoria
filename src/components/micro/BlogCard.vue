<script setup>
defineProps({
    blog: {
        type: Object,
        required: true
    }
})
</script>

<template>
    <div class="flex flex-col gap-3">
        <img :src="blog.image" alt="">
        <span class="flex items-center gap-2">
            <div class="py-2 px-4 rounded-3xl bg-primary-color text-center">
                <p class="text-small font-medium">{{ blog.category }}</p>
            </div>

            <p class="text-small font-medium">{{ blog.date }}</p>
        </span>
        <p class="text-body font-medium line-clamp-2">{{ blog.title }}</p>
    </div>
</template>