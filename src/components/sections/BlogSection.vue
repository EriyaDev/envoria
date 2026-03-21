<script setup>
import ButtonPrimary from '../micro/ButtonPrimary.vue'
import ButtonSecondary from '../micro/ButtonSecondary.vue'
</script>

<template>
    <div class="bg-[#f5f5f5] py-10">
        <div class="section-container mx-auto">
            <div class="flex items-end justify-between">
                <div class="flex flex-col gap-3 items-start">
                    <span
                        class="flex flex-row items-center w-fit px-3 py-1 bg-black/5 text-text-primary-color border border-[#2D612B]/13 text-small rounded-full font-semibold">
                        <div class="w-2 h-2 bg-accent-color rounded-full mr-2"></div>
                        Our Blog
                    </span>
                    <h2 class="medium-heading font-medium text-text-primary-color mt-10 text-start">
                        Inspiring insights for a <br>
                        smarter, <span class="text-text-primary-color/55">greener</span> future
                    </h2>
                </div>

                <div class="hidden md:flex">
                    <ButtonSecondary to="/blog" class="">
                        <p class="text-body font-medium">View All Blog</p>
                        <img src="../../assets/icons/home/arrow-white.svg" alt="" />
                    </ButtonSecondary>
                </div>
            </div>

            <!-- versi gapake slider -->
            <div class="grid grid-cols-1 md:grid-cols-2 mt-10 xl:grid-cols-3 gap-5">
                <div class="flex flex-col gap-3">
                    <img src="../../assets/images/blog/image-1.webp" alt="">
                    <span class="flex items-center gap-2">
                        <div class="py-2 px-4 rounded-3xl bg-primary-color text-center">
                            <p class="text-small font-medium">Zero Waste</p>
                        </div>

                        <p class="text-small font-medium">12 Mar 2026</p>
                    </span>
                    <p class="text-body font-medium line-clamp-2">Why Zero Waste Is More Than a Trend: A Complete Guide
                        to Low-Impact
                        Living</p>
                </div>

                <div class="flex flex-col gap-3">
                    <img src="../../assets/images/blog/image-2.webp" alt="">
                    <span class="flex items-center gap-2">
                        <div class="py-2 px-4 rounded-3xl bg-primary-color text-center">
                            <p class="text-small font-medium">Global Warming</p>
                        </div>

                        <p class="text-small font-medium">8 Mar 2026</p>
                    </span>
                    <p class="text-body font-medium line-clamp-2">Climate Facts 2025 Every Citizen Should Know</p>
                </div>

                <div class="flex flex-col gap-3">
                    <img src="../../assets/images/blog/image-3.webp" alt="">
                    <span class="flex items-center gap-2">
                        <div class="py-2 px-4 rounded-3xl bg-primary-color text-center">
                            <p class="text-small font-medium">Lifestyle</p>
                        </div>

                        <p class="text-small font-medium">4 Mar 2025</p>
                    </span>
                    <p class="text-body font-medium line-clamp-2">5 Eco-Friendly Switches Every Home Should Make</p>
                </div>
            </div>

            <div class="md:hidden mt-10 justify-center flex">
                <ButtonSecondary to="/blog" class="">
                    <p class="text-body font-medium">View All Blog</p>
                    <img src="../../assets/icons/home/arrow-white.svg" alt="" />
                </ButtonSecondary>
            </div>
        </div>
    </div>
</template>