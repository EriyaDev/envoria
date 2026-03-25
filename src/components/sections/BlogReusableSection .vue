<script setup>
import { onMounted } from 'vue'
import gsap from 'gsap'
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
];

let xPercent = 0

onMounted(() => {
    let currentScroll = 0
    let isScrollingDown = true

    let tween = gsap
        .to('.marquee__part', { xPercent: -100, repeat: -1, duration: 20, ease: 'linear' })
        .totalProgress(0.5)

    gsap.set('.marquee__inner', { xPercent: -50 })

    window.addEventListener('scroll', function () {
        if (window.pageYOffset > currentScroll) {
            isScrollingDown = true
        } else {
            isScrollingDown = false
        }

        gsap.to(tween, {
            timeScale: isScrollingDown ? 1 : -1,
        })

        currentScroll = window.pageYOffset
    })
})
</script>

<template>
    <div class="bg-card-color py-10">
        <div class="section-container mx-auto">
            <div class="flex items-center justify-between">
                <h2 class="medium-heading font-medium text-text-primary-color">
                    Recent Blog
                </h2>

                <div class="hidden md:flex">
                    <ButtonSecondary to="/blog" class="">
                        <p class="text-body font-medium">View All Blog</p>
                        <img src="../../assets/icons/home/arrow-white.svg" alt="" />
                    </ButtonSecondary>
                </div>
            </div>

            <!-- versi gapake slider -->
            <div class="grid grid-cols-1 md:grid-cols-2 mt-10 xl:grid-cols-3 gap-10 md:gap-5">
                <BlogCard v-for="blog in blogs" :key="blog.id" :blog="blog" />
            </div>

            <div class="w-[85%] mx-auto mt-10">
                <section class="marquee bg-primary-color rounded-2xl relative">
                    <div class="marquee__inner" aria-hidden="true" ref="inner">
                        <div class="marquee__part">
                            <img src="../../assets/images/testimonial/brand/brand-logo-batch.svg" class="pr-32"
                                alt="" />
                        </div>
                        <div class="marquee__part">
                            <img src="../../assets/images/testimonial/brand/brand-logo-batch.svg" class="pr-32"
                                alt="" />
                        </div>
                        <div class="marquee__part">
                            <img src="../../assets/images/testimonial/brand/brand-logo-batch.svg" class="pr-32"
                                alt="" />
                        </div>
                        <div class="marquee__part">
                            <img src="../../assets/images/testimonial/brand/brand-logo-batch.svg" class="pr-32"
                                alt="" />
                        </div>
                    </div>
                    <div
                        class="absolute h-full top-0 left-0 w-[100px] bg-linear-to-r from-card-color to-transparent pointer-events-none">
                    </div>
                    <div
                        class="absolute h-full top-0 right-0 w-[100px] bg-linear-to-l from-card-color to-transparent pointer-events-none">
                    </div>
                </section>
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

<style scoped>
.marquee__part {
    flex-shrink: 0;
    padding: 0 4px;
    font-smooth: always;
}

.marquee {
    color: #eee;
    text-transform: uppercase;
    font-weight: 600;
    font-size: 1.667vw;
    padding: 32px 0;

    position: relative;
    overflow: hidden;
}

.marquee__inner {
    -webkit-font-smoothing: antialiased;
    width: fit-content;
    display: flex;
    flex: auto;
    flex-direction: row;
}
</style>