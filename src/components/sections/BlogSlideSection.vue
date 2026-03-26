<script setup>
import { ref } from 'vue'
import ButtonPrimary from '../micro/ButtonPrimary.vue'
import ButtonSecondary from '../micro/ButtonSecondary.vue'
import { Swiper, SwiperSlide } from 'swiper/vue'
import { Navigation, Pagination, Autoplay } from 'swiper/modules'
import 'swiper/css'
import 'swiper/css/navigation'
import 'swiper/css/pagination'

const prevBtn = ref(null)
const nextBtn = ref(null)
</script>

<template>
    <div class="bg-[#F0F0F0] py-10 pt-32">
        <div class="section-container mx-auto">
            <div class="flex md:flex-row flex-col items-start gap-5 md:gap-0 md:items-end justify-between">
                <div class="flex flex-col gap-3 items-start">
                    <span
                        class="flex flex-row items-center w-fit px-3 py-1 bg-black/5 text-text-primary-color border border-[#2D612B]/13 text-small rounded-full font-semibold">
                        <div class="w-2 h-2 bg-accent-color rounded-full mr-2"></div>
                        Blog & Articles
                    </span>
                    <h2 class="medium-heading font-medium text-text-primary-color mt-10 text-start">
                        Stay <span class="text-text-primary-color/55">updated</span> with <br> Envoria latest <span
                            class="text-text-primary-color/55">news</span>

                    </h2>
                </div>

                <span class="flex items-center gap-5">
                    <button ref="prevBtn" class="button-secondary py-5! px-8!">
                        <img src="../../assets/icons/home/arrow-white.svg" alt="" class="rotate-180">
                    </button>

                    <button ref="nextBtn" class="button-secondary py-5! px-8!">
                        <img src="../../assets/icons/home/arrow-white.svg" alt="">
                    </button>
                </span>
            </div>

            <!-- versi pake slider -->
            <div class="mt-10">
                <Swiper :modules="[Navigation, Autoplay]" :slides-per-view="1" :space-between="20"
                    :navigation="{ prevEl: prevBtn, nextEl: nextBtn }" autoplay="{ delay: 3000 }"
                    class="w-full rounded-lg">
                    <SwiperSlide>
                        <div class="grid grid-cols-1 xl:grid-cols-10 gap-5">
                            <div class="xl:col-span-6">
                                <img src="../../assets/images/all-blog/image-1.png" alt=""
                                    class="h-full w-full object-cover rounded-xl">
                            </div>

                            <div class="xl:col-span-4 flex flex-col gap-3 bg-primary-color p-8 rounded-lg">
                                <span class="flex items-center gap-2">
                                    <div class="py-2 px-4 rounded-3xl bg-[#F0F0F0] text-center">
                                        <p class="text-small font-medium text-[#313131]">Zero Waste</p>
                                    </div>

                                    <p class="text-small font-medium">12 Mar 2026</p>
                                </span>
                                <h2 class="medium-heading font-medium line-clamp-3">Why Zero Waste Is More Than a Trend:
                                    A Complete
                                    Guide to
                                    Low-Impact Living</h2>
                                <p class="text-small font-medium line-clamp-5 text-[#464646]">Zero waste isn't just a
                                    lifestyle choice.
                                    it's a global movement reshaping how we consume, discard, and think about our
                                    planet. In this guide, we break down what low-impact living really means, why it
                                    matters more than ever, and how small daily changes can lead to a massive collective
                                    impact.</p>
                                <ButtonSecondary class="w-fit" to="/detail-blog">Read More</ButtonSecondary>
                            </div>
                        </div>
                    </SwiperSlide>

                    <SwiperSlide>
                        <div class="grid grid-cols-1 xl:grid-cols-10 gap-5">
                            <div class="xl:col-span-6">
                                <img src="../../assets/images/all-blog/image-1.png" alt=""
                                    class="h-full w-full object-cover rounded-xl">
                            </div>

                            <div class="xl:col-span-4 flex flex-col gap-3 bg-primary-color p-8 rounded-lg">
                                <span class="flex items-center gap-2">
                                    <div class="py-2 px-4 rounded-3xl bg-[#F0F0F0] text-center">
                                        <p class="text-small font-medium text-[#313131]">Zero Waste</p>
                                    </div>

                                    <p class="text-small font-medium">12 Mar 2026</p>
                                </span>
                                <h2 class="medium-heading font-medium line-clamp-3">Why Zero Waste Is More Than a Trend:
                                    A Complete
                                    Guide to
                                    Low-Impact Living</h2>
                                <p class="text-small font-medium line-clamp-5 text-[#464646]">Zero waste isn't just a
                                    lifestyle choice.
                                    it's a global movement reshaping how we consume, discard, and think about our
                                    planet. In this guide, we break down what low-impact living really means, why it
                                    matters more than ever, and how small daily changes can lead to a massive collective
                                    impact.</p>
                                <ButtonSecondary class="w-fit" to="/detail-blog">Read More</ButtonSecondary>
                            </div>
                        </div>
                    </SwiperSlide>

                </Swiper>
            </div>

        </div>
    </div>
</template>