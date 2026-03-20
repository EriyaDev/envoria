<script setup>
import ButtonPrimary from '@/components/micro/ButtonPrimary.vue'
</script>

<template>
    <section class="bg-third-color">
        <div class="section-container mx-auto py-10 md:px-0">
            <div class="flex flex-col justify-center items-center">
                <span
                    class="flex flex-row items-center w-fit px-3 py-1 bg-black text-white text-small rounded-full font-semibold border border-border-color">
                    <div class="w-2 h-2 bg-accent-color rounded-full mr-2 animate-pulse"></div>
                    Our Transportation
                </span>
                <h2 class="medium-heading font-medium text-center text-primary-color max-w-[50%] xl:max-w-[28%] mt-10">
                    Moving waste smarter,cleaner, and <span class="text-accent-color">faster.</span>
                </h2>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-0.5 mt-10">
                <div
                    class="flex flex-col items-center justify-center text-center gap-2 bg-fourth-color px-8 py-12 rounded-t-lg md:rounded-lg lg:rounded-l-lg lg:rounded-r-none">
                    <img src="../../assets/icons/home/hand.svg" alt="">
                    <h3 class="text-display font-bold text-accent-color">12k+</h3>
                    <p class="text-body font-semibold line-clamp-1 text-primary-color">Waste collected & transported
                        daily</p>
                </div>
                <div
                    class="flex flex-col items-center justify-center text-center gap-2 bg-fourth-color px-8 py-12 md:rounded-lg lg:rounded-none">
                    <img src="../../assets/icons/home/arrow-down.svg" alt="">
                    <h3 class="text-display font-bold text-accent-color">60%</h3>
                    <p class="text-body font-semibold line-clamp-1 text-primary-color">Emission reduction per route</p>
                </div>
                <div
                    class="flex flex-col items-center justify-center text-center gap-2 bg-fourth-color px-8 py-12 md:rounded-lg lg:rounded-none">
                    <img src="../../assets/icons/home/recycle.svg" alt="">
                    <h3 class="text-display font-bold text-accent-color">85%</h3>
                    <p class="text-body font-semibold line-clamp-1 text-primary-color">Recycling rate achieved</p>
                </div>
                <div
                    class="flex flex-col items-center justify-center text-center gap-2 bg-fourth-color px-8 py-12 rounded-b-lg md:rounded-lg lg:rounded-r-lg lg:rounded-l-none">
                    <img src="../../assets/icons/home/truck.svg" alt="">
                    <h3 class="text-display font-bold text-accent-color">2K+</h3>
                    <p class="text-body font-semibold line-clamp-1 text-primary-color">Active transport routes</p>
                </div>
            </div>

            <div class="grid grid-cols-1 xl:items-start xl:grid-cols-3 gap-5 mt-20">
                <div class="flex flex-col gap-10">
                    <div class="flex flex-col gap-2">
                        <p class="text-body text-accent-color">How We Transport Waste</p>
                        <h2 class="medium-heading font-extrabold text-primary-color">EFFICIENT WASTE MOVEMENT DRIVEN BY
                            <span class="text-accent-color">GREEN INNOVATION.</span>
                        </h2>
                    </div>

                    <p class="text-body text-text-third-color font-medium">Our system moves waste efficiently from
                        collection to
                        recycling using smart
                        logistics and sustainable transport methods.</p>

                    <ButtonPrimary class="w-fit">
                        <p class="text-body font-medium">Explore Service</p>
                        <img src="../../assets/icons/home/arrow-black.svg" alt="" />
                    </ButtonPrimary>
                </div>

                <div class="flex justify-center">
                    <img src="../../assets/images/transportation/image-1.png" alt="">
                </div>

                <div class="flex flex-col gap-10 items-center xl:items-start">
                    <p class="text-body text-text-third-color font-medium">Our system moves waste efficiently from
                        collection to
                        recycling using smart
                        logistics and sustainable transport methods.</p>

                    <div class="grid grid-cols-1 md:grid-cols-2 xl:grid-cols-1 gap-4">
                        <div
                            class="flex hover:bg-[#414141] hover:border-accent-color transition-all duration-300 cursor-pointer items-center gap-2 px-6 py-4 bg-[#0B0B0B] border border-[#363636] rounded-4xl">
                            <img src="../../assets/icons/home/arrow-down-green.svg" alt="">
                            <p class="text-body text-primary-color font-medium line-clamp-1">Low-emission compliance</p>
                        </div>
                        <div
                            class="flex hover:bg-[#414141] hover:border-accent-color transition-all duration-300 cursor-pointer items-center gap-2 px-6 py-4 bg-[#0B0B0B] border border-[#363636] rounded-4xl">
                            <img src="../../assets/icons/home/recycle-green.svg" alt="">
                            <p class="text-body text-primary-color font-medium line-clamp-1">Zero-waste recycling loop
                            </p>
                        </div>
                        <div
                            class="flex hover:bg-[#414141] hover:border-accent-color transition-all duration-300 cursor-pointer items-center gap-2 px-6 py-4 bg-[#0B0B0B] border border-[#363636] rounded-4xl">
                            <img src="../../assets/icons/home/clock-green.svg" alt="">
                            <p class="text-body text-primary-color font-medium line-clamp-1">Real-time cargo tracking
                            </p>
                        </div>
                        <div
                            class="flex hover:bg-[#414141] hover:border-accent-color transition-all duration-300 cursor-pointer items-center gap-2 px-6 py-4 bg-[#0B0B0B] border border-[#363636] rounded-4xl">
                            <img src="../../assets/icons/home/spark-green.svg" alt="">
                            <p class="text-body text-primary-color font-medium line-clamp-1">AI-powered route
                                optimization</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>
