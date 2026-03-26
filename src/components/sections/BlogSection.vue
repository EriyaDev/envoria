<script setup>
import ButtonPrimary from '../micro/ButtonPrimary.vue'
import ButtonSecondary from '../micro/ButtonSecondary.vue'
import BlogCard from '../micro/BlogCard.vue'

const blogs = [
  {
    id: 1,
    title: 'Why Zero Waste Is More Than a Trend: A Complete Guide To Low-Impact Living',
    category: 'Zero Waste',
    date: '12 Mar 2026',
    image: new URL('../../assets/images/blog/image-1.webp', import.meta.url).href,
  },
  {
    id: 2,
    title: 'Climate Facts 2025 Every Citizen Should Know',
    category: 'Global Warming',
    date: '8 Mar 2026',
    image: new URL('../../assets/images/blog/image-2.webp', import.meta.url).href,
  },
  {
    id: 3,
    title: '5 Eco-Friendly Switches Every Home Should Make',
    category: 'Lifestyle',
    date: '4 Mar 2026',
    image: new URL('../../assets/images/blog/image-3.webp', import.meta.url).href,
  },
]
</script>

<template>
  <div class="bg-card-color py-10">
    <div class="section-container mx-auto">
      <div class="flex items-end justify-between">
        <div class="flex flex-col gap-3 items-start">
          <span
            class="flex flex-row items-center w-fit px-3 py-1 bg-black/5 text-text-primary-color border border-[#2D612B]/13 text-small rounded-full font-semibold"
          >
            <div class="w-2 h-2 bg-accent-color rounded-full mr-2"></div>
            Our Blog
          </span>
          <h2
            data-aos="fade-right"
            data-aos-delay="00"
            class="medium-heading font-medium text-text-primary-color mt-10 text-start"
          >
            Inspiring insights for a <br />
            smarter, <span class="text-text-primary-color/55">greener</span> future
          </h2>
        </div>

        <div data-aos="fade-left" data-aos-delay="00" class="hidden md:flex">
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

      <div class="md:hidden mt-10 justify-center flex">
        <ButtonSecondary to="/blog" class="">
          <p class="text-body font-medium">View All Blog</p>
          <img src="../../assets/icons/home/arrow-white.svg" alt="" />
        </ButtonSecondary>
      </div>
    </div>
  </div>
</template>
