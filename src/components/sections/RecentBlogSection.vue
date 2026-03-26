<script setup>
import ButtonPrimary from '../micro/ButtonPrimary.vue'
import ButtonSecondary from '../micro/ButtonSecondary.vue'
import BlogCard from '../micro/BlogCard.vue'

const blogs = [
    {
        id: 1,
        title: "Why Zero Waste Is More Than a Trend: A Complete Guide To Low-Impact Living",
        category: "Zero Waste",
        date: "12 Mar 2026",
        image: new URL('../../assets/images/blog/image-1.webp', import.meta.url).href,
    },
    {
        id: 2,
        title: "Climate Facts 2025 Every Citizen Should Know",
        category: "Global Warming",
        date: "8 Mar 2026",
        image: new URL('../../assets/images/blog/image-2.webp', import.meta.url).href,
    },
    {
        id: 3,
        title: "5 Eco-Friendly Switches Every Home Should Make",
        category: "Lifestyle",
        date: "4 Mar 2026",
        image: new URL('../../assets/images/blog/image-3.webp', import.meta.url).href,

    },
    {
        id: 4,
        title: "Indonesia’s Most Endangered Ecosystems And What We Can Do About It",
        category: "Biodiversity",
        date: "28 Feb 2026",
        image: new URL('../../assets/images/blog/image-4.webp', import.meta.url).href,
    },
    {
        id: 5,
        title: "The Plastic Crisis In Our Oceans Is Worse Than You Think",
        category: "Marine",
        date: "22 Feb 2026",
        image: new URL('../../assets/images/blog/image-5.webp', import.meta.url).href,
    },
    {
        id: 6,
        title: "How To Build A Zero-Waste Kitchen In 30 Days",
        category: "Lifestyle",
        date: "8 Feb 2026",
        image: new URL('../../assets/images/blog/image-6.webp', import.meta.url).href,
    }
];
</script>

<template>
    <div class="py-10 bg-[#F5F5F5]">
        <div class="section-container mx-auto">
            <div class="flex flex-col gap-5">
                <div class="flex flex-col gap-3 items-start">
                    <span
                        class="flex flex-row items-center w-fit px-3 py-1 bg-black/5 text-text-primary-color border border-[#2D612B]/13 text-small rounded-full font-semibold">
                        <div class="w-2 h-2 bg-accent-color rounded-full mr-2"></div>
                        Recent Blog & Articles
                    </span>
                    <h2 class="medium-heading font-medium text-text-primary-color mt-10 text-start">
                        Latest <span class="text-text-primary-color/55">insights</span> and <br> <span
                            class="text-text-primary-color/55">trends</span>
                    </h2>
                </div>

                <div class="flex items-center gap-4">
                    <button class="button-secondary">All Topics</button>
                    <button class="button-outline">Zero Waste</button>
                    <button class="button-outline">Global Warming</button>
                    <button class="button-outline">Lifestyle</button>
                    <button class="button-primary">+9 More</button>
                </div>
            </div>

            <!-- versi gapake slider -->
            <div class="grid grid-cols-1 md:grid-cols-2 mt-10 xl:grid-cols-3 gap-10 md:gap-5">
                <BlogCard v-for="blog in blogs" :key="blog.id" :blog="blog" />
            </div>

            <div class="mt-10 justify-center flex">
                <ButtonPrimary to="/blog" class="">
                    <p class="text-body font-medium">Load More</p>
                </ButtonPrimary>
            </div>
        </div>
    </div>
</template>