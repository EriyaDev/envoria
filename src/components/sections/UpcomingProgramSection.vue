<script setup>
import ButtonPrimary from '../micro/ButtonPrimary.vue'
import ButtonSecondary from '../micro/ButtonSecondary.vue'
import { Swiper, SwiperSlide } from 'swiper/vue'
import { Navigation, Pagination, Autoplay } from 'swiper/modules'
import 'swiper/css'
import 'swiper/css/navigation'
import 'swiper/css/pagination'
</script>

<template>
    <div class="bg-[#f5f5f5] py-10">
        <div class="section-container mx-auto">
            <div class="flex items-end justify-between">
                <div class="flex flex-col gap-3 items-start">
                    <span
                        class="flex flex-row items-center w-fit px-3 py-1 bg-black/5 text-text-primary-color border border-[#2D612B]/13 text-small rounded-full font-semibold">
                        <div class="w-2 h-2 bg-accent-color rounded-full mr-2"></div>
                        Upcoming Programs
                    </span>
                    <h2
                        class="medium-heading font-medium text-text-primary-color mt-10 text-start md:max-w-[70%] xl:max-w-[37%]">
                        Our Real-World <br> Action
                        <span class="text-text-primary-color/55">Programs</span>
                    </h2>
                    <p class="text-body font-medium text-text-third-color mt-3 md:max-w-[70%]">
                        Every program, every volunteer, and every tree we plant is living proof that collective
                        action reshapes the environment one small step at a time.
                    </p>
                </div>

                <div class="hidden lg:flex">
                    <ButtonSecondary to="/programs" class="">
                        <p class="text-body font-medium">See All Programs</p>
                        <img src="../../assets/icons/home/arrow-white.svg" alt="" />
                    </ButtonSecondary>
                </div>
            </div>

            <!-- versi pake slider -->
            <!-- <div class="mt-10">
                <Swiper :modules="[Navigation, Pagination, Autoplay]" :slides-per-view="2" :space-between="20"
                    :navigation="false" :pagination="{ clickable: true }"
                    :autoplay="{ delay: 3000, disableOnInteraction: false }" :loop="true" class="w-full rounded-lg">
                    <SwiperSlide>
                        <div class="grid grid-cols-1 md:grid-cols-10 p-5 rounded-lg bg-primary-color gap-5">
                            <div class="md:col-span-6 gap-10 flex flex-col order-last md:order-first">
                                <span
                                    class="flex flex-row items-center w-fit px-3 py-1 bg-accent-color/16 text-text-primary-color border border-border-color/55 text-small rounded-full font-semibold">
                                    <div class="w-2 h-2 bg-accent-color rounded-full mr-2"></div>
                                    Active Now
                                </span>

                                <div class="flex flex-col gap-2">
                                    <h2 class="small-heading font-medium">Borneo Forest Reforestation 2026</h2>
                                    <p class="text-small text-text-third-color">A program to plant 10,000 endemic trees
                                        in critical lands of
                                        Central
                                        Kalimantan with
                                        local communities.</p>
                                </div>

                                <div class="border border-dashed border-[#8E8E8E] flex flex-col gap-2 p-3 rounded-lg">
                                    <span class="flex items-center gap-2">
                                        <img src="../../assets/icons/home/calendar.svg" alt="" />
                                        <span class="text-small text-text-third-color font-medium">15 Mar - 30 Jun
                                            2026</span>
                                    </span>

                                    <div class="w-full">
                                        <div
                                            class="w-full h-3 bg-[#DBDBDB] rounded-full overflow-hidden border border-gray-200">
                                            <div class="h-full bg-accent-color rounded-full" style="width: 87%"></div>
                                        </div>
                                    </div>

                                    <span class="flex items-center justify-between gap-2">
                                        <span class="text-small text-text-third-color font-medium">6.700 / 10.000
                                            Tree</span>
                                        <span class="text-small text-text-third-color font-medium">67%</span>
                                    </span>
                                </div>

                                <ButtonPrimary class="w-fit">
                                    <p class="text-body font-medium">Sign Up Now</p>
                                    <img src="../../assets/icons/home/arrow-black.svg" alt="" />
                                </ButtonPrimary>
                            </div>
                            <div class="md:col-span-4 h-52 md:h-full w-full order-first md:order-last">
                                <img src="../../assets/images/upcoming-program/image-1.svg" alt=""
                                    class="h-full w-full object-cover rounded-lg">
                            </div>
                        </div>
                    </SwiperSlide>

                    <SwiperSlide>
                        <div class="grid grid-cols-1 md:grid-cols-10 p-5 rounded-lg bg-primary-color gap-5">
                            <div class="md:col-span-6 gap-10 flex flex-col order-last md:order-first">
                                <span
                                    class="flex flex-row items-center w-fit px-3 py-1 bg-accent-color/16 text-text-primary-color border border-border-color/55 text-small rounded-full font-semibold">
                                    <div class="w-2 h-2 bg-accent-color rounded-full mr-2"></div>
                                    Active Now
                                </span>

                                <div class="flex flex-col gap-2">
                                    <h2 class="small-heading font-medium">Borneo Forest Reforestation 2026</h2>
                                    <p class="text-small text-text-third-color">A program to plant 10,000 endemic trees
                                        in critical lands of
                                        Central
                                        Kalimantan with
                                        local communities.</p>
                                </div>

                                <div class="border border-dashed border-[#8E8E8E] flex flex-col gap-2 p-3 rounded-lg">
                                    <span class="flex items-center gap-2">
                                        <img src="../../assets/icons/home/calendar.svg" alt="" />
                                        <span class="text-small text-text-third-color font-medium">15 Mar - 30 Jun
                                            2026</span>
                                    </span>

                                    <div class="w-full">
                                        <div
                                            class="w-full h-3 bg-[#DBDBDB] rounded-full overflow-hidden border border-gray-200">
                                            <div class="h-full bg-accent-color rounded-full" style="width: 87%"></div>
                                        </div>
                                    </div>

                                    <span class="flex items-center justify-between gap-2">
                                        <span class="text-small text-text-third-color font-medium">6.700 / 10.000
                                            Tree</span>
                                        <span class="text-small text-text-third-color font-medium">67%</span>
                                    </span>
                                </div>

                                <ButtonPrimary class="w-fit">
                                    <p class="text-body font-medium">Sign Up Now</p>
                                    <img src="../../assets/icons/home/arrow-black.svg" alt="" />
                                </ButtonPrimary>
                            </div>
                            <div class="md:col-span-4 h-52 md:h-full w-full order-first md:order-last">
                                <img src="../../assets/images/upcoming-program/image-1.svg" alt=""
                                    class="h-full w-full object-cover rounded-lg">
                            </div>
                        </div>
                    </SwiperSlide>

                    <SwiperSlide>
                        <div class="grid grid-cols-1 md:grid-cols-10 p-5 rounded-lg bg-primary-color gap-5">
                            <div class="md:col-span-6 gap-10 flex flex-col order-last md:order-first">
                                <span
                                    class="flex flex-row items-center w-fit px-3 py-1 bg-accent-color/16 text-text-primary-color border border-border-color/55 text-small rounded-full font-semibold">
                                    <div class="w-2 h-2 bg-accent-color rounded-full mr-2"></div>
                                    Active Now
                                </span>

                                <div class="flex flex-col gap-2">
                                    <h2 class="small-heading font-medium">Borneo Forest Reforestation 2026</h2>
                                    <p class="text-small text-text-third-color">A program to plant 10,000 endemic trees
                                        in critical lands of
                                        Central
                                        Kalimantan with
                                        local communities.</p>
                                </div>

                                <div class="border border-dashed border-[#8E8E8E] flex flex-col gap-2 p-3 rounded-lg">
                                    <span class="flex items-center gap-2">
                                        <img src="../../assets/icons/home/calendar.svg" alt="" />
                                        <span class="text-small text-text-third-color font-medium">15 Mar - 30 Jun
                                            2026</span>
                                    </span>

                                    <div class="w-full">
                                        <div
                                            class="w-full h-3 bg-[#DBDBDB] rounded-full overflow-hidden border border-gray-200">
                                            <div class="h-full bg-accent-color rounded-full" style="width: 87%"></div>
                                        </div>
                                    </div>

                                    <span class="flex items-center justify-between gap-2">
                                        <span class="text-small text-text-third-color font-medium">6.700 / 10.000
                                            Tree</span>
                                        <span class="text-small text-text-third-color font-medium">67%</span>
                                    </span>
                                </div>

                                <ButtonPrimary class="w-fit">
                                    <p class="text-body font-medium">Sign Up Now</p>
                                    <img src="../../assets/icons/home/arrow-black.svg" alt="" />
                                </ButtonPrimary>
                            </div>
                            <div class="md:col-span-4 h-52 md:h-full w-full order-first md:order-last">
                                <img src="../../assets/images/upcoming-program/image-1.svg" alt=""
                                    class="h-full w-full object-cover rounded-lg">
                            </div>
                        </div>
                    </SwiperSlide>
                </Swiper>
            </div> -->

            <!-- versi gapake slider -->
            <div class="grid grid-cols-1 mt-10 xl:grid-cols-2 gap-5">
                <div class="grid grid-cols-1 md:grid-cols-10 p-5 rounded-lg bg-primary-color gap-5">
                    <div class="md:col-span-6 gap-10 flex flex-col order-last md:order-first">
                        <span
                            class="flex flex-row items-center w-fit px-3 py-1 bg-accent-color/16 text-text-primary-color border border-border-color/55 text-small rounded-full font-semibold">
                            <div class="w-2 h-2 bg-accent-color rounded-full mr-2"></div>
                            Active Now
                        </span>

                        <div class="flex flex-col gap-2">
                            <h2 class="small-heading font-medium">Borneo Forest Reforestation 2026</h2>
                            <p class="text-small text-text-third-color line-clamp-2">A program to plant 10,000 endemic
                                trees
                                in critical lands of
                                Central
                                Kalimantan with
                                local communities.</p>
                        </div>

                        <div class="border border-dashed border-[#8E8E8E] flex flex-col gap-2 p-3 rounded-lg">
                            <span class="flex items-center gap-2">
                                <img src="../../assets/icons/home/calendar.svg" alt="" />
                                <span class="text-small text-text-third-color font-medium">15 Mar - 30 Jun
                                    2026</span>
                            </span>

                            <div class="w-full">
                                <div
                                    class="w-full h-3 bg-[#DBDBDB] rounded-full overflow-hidden border border-gray-200">
                                    <div class="h-full bg-accent-color rounded-full" style="width: 87%"></div>
                                </div>
                            </div>

                            <span class="flex items-center justify-between gap-2">
                                <span class="text-small text-text-third-color font-medium">6.700 / 10.000
                                    Tree</span>
                                <span class="text-small text-text-third-color font-medium">67%</span>
                            </span>
                        </div>

                        <ButtonPrimary class="w-fit">
                            <p class="text-body font-medium">Sign Up Now</p>
                            <img src="../../assets/icons/home/arrow-black.svg" alt="" />
                        </ButtonPrimary>
                    </div>
                    <div class="md:col-span-4 h-52 md:h-full w-full order-first md:order-last">
                        <img src="../../assets/images/upcoming-program/image-1.svg" alt=""
                            class="h-full w-full object-cover rounded-lg">
                    </div>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-10 p-5 rounded-lg bg-primary-color gap-5">
                    <div class="md:col-span-6 gap-10 flex flex-col order-last md:order-first">
                        <span
                            class="flex flex-row items-center w-fit px-3 py-1 bg-[#FFBB5B]/16 text-text-primary-color border border-[#61592B]/13 text-small rounded-full font-semibold">
                            <div class="w-2 h-2 bg-[#8B1C00] rounded-full mr-2"></div>
                            Coming Soon
                        </span>

                        <div class="flex flex-col gap-2">
                            <h2 class="small-heading font-medium">Clean-Up Pantai Bali 2026</h2>
                            <p class="text-small text-text-third-color line-clamp-2">A mass beach cleanup took place in
                                five
                                locations in Bali. The goal was to remove 3 tons of plastic waste from the coast.</p>
                        </div>

                        <div class="border border-dashed border-[#8E8E8E] flex flex-col gap-2 p-3 rounded-lg">
                            <span class="flex items-center gap-2">
                                <img src="../../assets/icons/home/calendar.svg" alt="" />
                                <span class="text-small text-text-third-color font-medium">20 Mar - 30 July 2026</span>
                            </span>

                            <div class="w-full">
                                <div
                                    class="w-full h-3 bg-[#DBDBDB] rounded-full overflow-hidden border border-gray-200">
                                    <div class="h-full bg-accent-color rounded-full" style="width: 0%"></div>
                                </div>
                            </div>

                            <span class="flex items-center justify-between gap-2">
                                <span class="text-small text-text-third-color font-medium">0 / 100 Units</span>
                                <span class="text-small text-text-third-color font-medium">0%</span>
                            </span>
                        </div>

                        <ButtonPrimary class="w-fit">
                            <p class="text-body font-medium">Sign Up Now</p>
                            <img src="../../assets/icons/home/arrow-black.svg" alt="" />
                        </ButtonPrimary>
                    </div>
                    <div class="md:col-span-4 h-52 md:h-full w-full order-first md:order-last">
                        <img src="../../assets/images/upcoming-program/image-2.svg" alt=""
                            class="h-full w-full object-cover rounded-lg">
                    </div>
                </div>
            </div>

            <div class="lg:hidden mt-10 justify-center flex">
                <ButtonSecondary to="/programs" class="">
                    <p class="text-body font-medium">See All Programs</p>
                    <img src="../../assets/icons/home/arrow-white.svg" alt="" />
                </ButtonSecondary>
            </div>
        </div>
    </div>
</template>