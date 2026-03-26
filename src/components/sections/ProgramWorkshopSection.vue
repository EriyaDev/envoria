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
                    Seminars & Workshops
                </span>
                <h2 class="medium-heading font-medium text-text-primary-color mt-10 text-start">
                    Learn <span class="text-text-primary-color/55">directly</span> from
                    <br>
                    the experts.
                </h2>
            </div>

            <!-- versi gapake slider -->
            <div class="grid grid-cols-1 mt-10 gap-5">
                <div class="grid grid-cols-1 lg:grid-cols-10 p-5 rounded-lg bg-primary-color gap-5">
                    <div class="lg:col-span-4 w-full h-100 lg:h-full xl:h-125">
                        <img src="../../assets/images/upcoming-program/image-1.svg" alt=""
                            class="h-full w-full object-cover rounded-lg">
                    </div>

                    <div class="lg:col-span-6 gap-10 flex flex-col">
                        <span
                            class="flex flex-row items-center w-fit px-3 py-1 bg-accent-color/16 text-text-primary-color border border-border-color/55 text-small rounded-full font-semibold">
                            <div class="w-2 h-2 bg-accent-color rounded-full mr-2"></div>
                            Crisis
                        </span>

                        <div class="flex flex-col gap-2">
                            <h2 class="small-heading font-medium">National Seminar: Climate Crisis & Indonesian Food
                                Security 2050</h2>
                            <p class="text-small text-text-third-color line-clamp-2">An in-depth discussion on the
                                impacts of climate change on agricultural productivity and the long-term adaptation
                                strategies that need to be prepared now.</p>
                        </div>

                        <div
                            class="border text-nowrap overflow-x-scroll w-full border-dashed border-[#8E8E8E] flex flex-col gap-2 p-5 rounded-lg">
                            <div class="flex items-center gap-10 lg:gap-5">
                                <span class="flex items-center gap-2">
                                    <img src="../../assets/icons/home/location.svg" alt="" />
                                    <span class="text-small text-text-third-color font-medium">Auditorium UI,
                                        Depok</span>
                                </span>

                                <span class="flex items-center gap-2">
                                    <img src="../../assets/icons/home/group-outline.svg" alt="" />
                                    <span class="text-small text-text-third-color font-medium">+500 Seats</span>
                                </span>

                                <span class="flex items-center gap-2">
                                    <img src="../../assets/icons/home/clock.svg" alt="" />
                                    <span class="text-small text-text-third-color font-medium">08.00 – 17.00 WIB</span>
                                </span>

                                <span class="flex items-center gap-2">
                                    <img src="../../assets/icons/home/ticket.svg" alt="" />
                                    <span class="text-small text-text-third-color font-medium">Free</span>
                                </span>
                            </div>

                            <div class="border-b border-[#8E8E8E] w-full border-dashed"></div>

                            <span class="flex items-center gap-2">
                                <img src="../../assets/icons/home/calendar.svg" alt="" />
                                <span class="text-small text-text-third-color font-medium">March 20</span>
                            </span>

                        </div>

                        <span class="flex items-center gap-5">
                            <div class="p-4 rounded-4xl flex bg-[#F5F5F5] items-center gap-2">
                                <img src="../../assets/profile/mira.svg" alt="">
                                <p class="text-body">Prof. Mira S.</p>
                            </div>

                            <div class="p-4 rounded-4xl flex bg-[#F5F5F5] items-center gap-2">
                                <img src="../../assets/profile/dini.svg" alt="">
                                <p class="text-body">Dini M., Blogger</p>
                            </div>
                        </span>

                        <ButtonPrimary class="w-fit">
                            <p class="text-body font-medium">Register For Free</p>
                            <img src="../../assets/icons/home/arrow-black.svg" alt="" />
                        </ButtonPrimary>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>