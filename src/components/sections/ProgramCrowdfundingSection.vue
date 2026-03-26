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
                    Crowdfunding
                </span>
                <h2 class="medium-heading font-medium text-text-primary-color mt-10 text-start">
                    Every dollar
                    <br>
                    <span class="text-text-primary-color/55">counts.</span>
                </h2>
            </div>

            <!-- versi gapake slider -->
            <div class="grid grid-cols-1 mt-10 xl:grid-cols-2 gap-5">
                <div class="grid xl:col-span-2 grid-cols-1 md:grid-cols-10 p-5 rounded-lg bg-primary-color gap-5">
                    <div class="md:col-span-5 h-100 w-full">
                        <img src="../../assets/images/program-crowdfunding/image-1.webp" alt=""
                            class="h-full w-full object-cover rounded-lg">
                    </div>

                    <div class="md:col-span-5 gap-10 flex flex-col">
                        <div class="flex items-center gap-5">
                            <span
                                class="flex flex-row items-center w-fit px-3 py-1 bg-[#FFF3F3] text-[#FF6666] border border-[#6C0000]/55 text-small rounded-full font-semibold">
                                <div class="w-2 h-2 bg-[#FF3030] rounded-full mr-2"></div>
                                ACTIVE - Running Now
                            </span>
                            <span
                                class="flex flex-row items-center w-fit px-3 py-1 bg-[#FFF3F3] text-[#FF6666] border border-[#6C0000]/55 text-small rounded-full font-semibold">
                                <div class="w-2 h-2 bg-[#FF3030] rounded-full mr-2"></div>
                                3 Days Left
                            </span>
                        </div>

                        <div class="flex flex-col gap-2">
                            <h2 class="small-heading font-medium">Emergency Fund for Forest Recovery After the Riau
                                Fires</h2>
                            <p class="text-small text-text-third-color line-clamp-2">More than 2,000 hectares of Riau's
                                peatland forests have burned. EcoNusa is launching an emergency fundraising campaign to
                                cover land rehabilitation costs and the recovery of affected wildlife.</p>
                        </div>

                        <div class="border border-dashed border-[#8E8E8E] flex flex-col gap-2 p-3 rounded-lg">
                            <span class="flex items-center gap-2">
                                <img src="../../assets/icons/home/group-outline-2.svg" alt="" />
                                <span class="text-small text-text-third-color font-medium">+1,236 others joined</span>
                            </span>

                            <div class="w-full">
                                <div
                                    class="w-full h-3 bg-[#DBDBDB] rounded-full overflow-hidden border border-gray-200">
                                    <div class="h-full bg-accent-color rounded-full" style="width: 76%"></div>
                                </div>
                            </div>

                            <span class="flex items-center justify-between gap-2">
                                <span class="text-small text-text-third-color font-medium">$25,677.87 / $30,000</span>
                                <span class="text-small text-text-third-color font-medium">76%</span>
                            </span>
                        </div>

                        <ButtonPrimary class="w-fit">
                            <img src="../../assets/icons/home/heart.svg" alt="" />
                            <p class="text-body font-medium">Donate Now</p>
                        </ButtonPrimary>
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
                            <h2 class="small-heading font-medium">Procurement of Professional Beach Cleaning Equipment
                            </h2>
                            <p class="text-small text-text-third-color line-clamp-2">Purchased nets, gloves, and safety
                                equipment for 200 beach clean-up volunteers.</p>
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
                                <span class="text-small text-text-third-color font-medium">$1,230.00 / $1,600.00</span>
                                <span class="text-small text-text-third-color font-medium">85%</span>
                            </span>
                        </div>

                        <ButtonPrimary class="w-fit">
                            <img src="../../assets/icons/home/heart.svg" alt="" />
                            <p class="text-body font-medium">Donate Now</p>
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
                            Active Now
                        </span>

                        <div class="flex flex-col gap-2">
                            <h2 class="small-heading font-medium">Raja Ampat Coral Reef Seeds
                            </h2>
                            <p class="text-small text-text-third-color line-clamp-2">Purchase of 500 coral reef
                                fragments from an official nursery for an underwater rehabilitation program.</p>
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
                                <span class="text-small text-text-third-color font-medium">$1,230.00 / $1,600.00</span>
                                <span class="text-small text-text-third-color font-medium">85%</span>
                            </span>
                        </div>

                        <ButtonPrimary class="w-fit">
                            <img src="../../assets/icons/home/heart.svg" alt="" />
                            <p class="text-body font-medium">Donate Now</p>
                        </ButtonPrimary>
                    </div>
                    <div class="md:col-span-4 h-52 md:h-full w-full order-first md:order-last">
                        <img src="../../assets/images/upcoming-program/image-3.webp" alt=""
                            class="h-full w-full object-cover rounded-lg">
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>