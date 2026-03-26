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
    <div class="bg-card-color py-10">
        <div class="section-container mx-auto">
            <div class="flex flex-col gap-3 items-start">
                <span
                    class="flex flex-row items-center w-fit px-3 py-1 bg-black/5 text-text-primary-color border border-[#2D612B]/13 text-small rounded-full font-semibold">
                    <div class="w-2 h-2 bg-accent-color rounded-full mr-2"></div>
                    Action Program
                </span>
                <h2 class="medium-heading font-medium text-text-primary-color mt-10 text-start">
                    Real action
                    <br> on
                    <span class="text-text-primary-color/55">the ground.</span>
                </h2>

                <div class="flex items-center w-full overflow-x-auto text-nowrap gap-4">
                    <button class="button-secondary">All Programs</button>
                    <button class="button-white">Ongoing</button>
                    <button class="button-white">Coming Soon</button>
                    <button class="button-white">Completed</button>
                </div>
            </div>

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

                <div class="grid grid-cols-1 md:grid-cols-10 p-5 rounded-lg bg-primary-color gap-5">
                    <div class="md:col-span-6 gap-10 flex flex-col order-last md:order-first">
                        <span
                            class="flex flex-row items-center w-fit px-3 py-1 bg-accent-color/16 text-text-primary-color border border-border-color/55 text-small rounded-full font-semibold">
                            <div class="w-2 h-2 bg-accent-color rounded-full mr-2"></div>
                            Active Now
                        </span>

                        <div class="flex flex-col gap-2">
                            <h2 class="small-heading font-medium">Indonesian Waste Bank</h2>
                            <p class="text-small text-text-third-color line-clamp-2">Expansion of the waste bank network
                                to 100 new points in Java and Sulawesi.</p>
                        </div>

                        <div class="border border-dashed border-[#8E8E8E] flex flex-col gap-2 p-3 rounded-lg">
                            <span class="flex items-center gap-2">
                                <img src="../../assets/icons/home/calendar.svg" alt="" />
                                <span class="text-small text-text-third-color font-medium">Jan - Dec 2026</span>
                            </span>

                            <div class="w-full">
                                <div
                                    class="w-full h-3 bg-[#DBDBDB] rounded-full overflow-hidden border border-gray-200">
                                    <div class="h-full bg-accent-color rounded-full" style="width: 85%"></div>
                                </div>
                            </div>

                            <span class="flex items-center justify-between gap-2">
                                <span class="text-small text-text-third-color font-medium">149 / 200 Units</span>
                                <span class="text-small text-text-third-color font-medium">85%</span>
                            </span>
                        </div>

                        <ButtonPrimary class="w-fit">
                            <p class="text-body font-medium">Sign Up Now</p>
                            <img src="../../assets/icons/home/arrow-black.svg" alt="" />
                        </ButtonPrimary>
                    </div>
                    <div class="md:col-span-4 h-52 md:h-full w-full order-first md:order-last">
                        <img src="../../assets/images/upcoming-program/image-3.webp" alt=""
                            class="h-full w-full object-cover rounded-lg">
                    </div>
                </div>

                <div class="grid grid-cols-1 md:grid-cols-10 p-5 rounded-lg bg-primary-color gap-5">
                    <div class="md:col-span-6 gap-10 flex flex-col order-last md:order-first">
                        <span
                            class="flex flex-row items-center w-fit px-3 py-1 bg-accent-color/16 text-text-primary-color border border-border-color/55 text-small rounded-full font-semibold">
                            <div class="w-2 h-2 bg-accent-color rounded-full mr-2"></div>
                            Finished
                        </span>

                        <div class="flex flex-col gap-2">
                            <h2 class="small-heading font-medium">Urban Farming Jakarta 2025</h2>
                            <p class="text-small text-text-third-color line-clamp-2">An urban farming program in 50
                                locations in Jakarta has successfully produced 2 tons of organic vegetables.</p>
                        </div>

                        <div class="border border-dashed border-[#8E8E8E] flex flex-col gap-2 p-3 rounded-lg">
                            <span class="flex items-center gap-2">
                                <img src="../../assets/icons/home/calendar.svg" alt="" />
                                <span class="text-small text-text-third-color font-medium">Finished on dec 2025</span>
                            </span>

                            <div class="w-full">
                                <div
                                    class="w-full h-3 bg-[#DBDBDB] rounded-full overflow-hidden border border-gray-200">
                                    <div class="h-full bg-accent-color rounded-full" style="width: 100%"></div>
                                </div>
                            </div>

                            <span class="flex items-center justify-between gap-2">
                                <span class="text-small text-text-third-color font-medium">50 / 50 Units</span>
                                <span class="text-small text-text-third-color font-medium">100%</span>
                            </span>
                        </div>

                        <button class="button-outline flex items-center gap-2 w-fit">See Report <img
                                src="../../assets/icons/home/arrow-black.svg" alt=""></button>
                    </div>
                    <div class="md:col-span-4 h-52 md:h-full w-full order-first md:order-last">
                        <img src="../../assets/images/upcoming-program/image-4.webp" alt=""
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