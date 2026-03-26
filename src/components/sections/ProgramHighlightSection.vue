<script setup>
import { ref } from 'vue'
import ButtonPrimary from '../micro/ButtonPrimary.vue'
import ButtonSecondary from '../micro/ButtonSecondary.vue'
</script>

<template>
    <div class="bg-[#F5F5F5] py-10">
        <div class="section-container mx-auto">
            <span
                class="flex flex-row items-center w-fit px-3 py-1 bg-black/5 text-text-primary-color border border-[#2D612B]/13 text-small rounded-full font-semibold">
                <div class="w-2 h-2 bg-accent-color rounded-full mr-2"></div>
                Highlights
            </span>

            <div data-aos="fade-up" data-aos-delay="200" class="grid grid-cols-1 xl:grid-cols-10 gap-5 mt-10">
                <div class="xl:col-span-6 relative overflow-hidden h-120">
                    <div class="absolute inset-0">
                        <img src="../../assets/images/program-highlight/image-1.webp" alt=""
                            class="h-full w-full object-cover rounded-xl">
                    </div>

                    <div class="absolute inset-0 p-10 flex flex-col gap-5">
                        <span
                            class="flex flex-row items-center w-fit px-3 py-1 bg-[#FFF3F3] text-[#FF6666] border border-[#2D612B]/13 text-small rounded-full font-semibold">
                            <div class="w-2 h-2 bg-[#FF6666] rounded-full mr-2"></div>
                            ACTIVE - Running Now
                        </span>
                        <h2 class="medium-heading max-w-[70%] font-extrabold text-primary-color">Emergency Fund for
                            Forest Recovery
                            After the Riau Fires</h2>
                        <p class="text-small text-primary-color">More than 2,000 hectares of Riau's peatland forests
                            have
                            burned.
                            EcoNusa is launching an emergency fundraising campaign to cover land rehabilitation
                            costs and the recovery of affected wildlife.</p>
                    </div>
                </div>

                <div class="xl:col-span-4 flex flex-col gap-8 justify-center bg-primary-color p-8 rounded-lg">
                    <h4 class="small-heading text-[#313131]">TOTAL COLLECTED</h4>
                    <div class="flex flex-col gap-2">
                        <h2 class="medium-heading font-extrabold">$25,677.87</h2>
                        <span class="flex items-center gap-5">
                            <img src="../../assets/icons/home/clock-red.svg" alt="">
                            <p class="text-body text-[#FF6666]">3 days left to help before it's too late!</p>
                        </span>
                    </div>
                    <div class="border border-dashed border-[#8E8E8E] flex flex-col gap-2 p-3 rounded-lg">
                        <span class="flex items-center gap-2">
                            <img src="../../assets/icons/home/group-outline.svg" alt="" />
                            <span class="text-small text-text-third-color font-medium">+1,236 others joined</span>
                        </span>

                        <div class="w-full">
                            <div class="w-full h-3 bg-[#DBDBDB] rounded-full overflow-hidden border border-gray-200">
                                <div class="h-full bg-accent-color rounded-full" style="width: 76%"></div>
                            </div>
                        </div>

                        <span class="flex items-center justify-between gap-2">
                            <span class="text-small text-text-third-color font-medium">$25,677.87 / $30,000</span>
                            <span class="text-small text-text-third-color font-medium">76%</span>
                        </span>
                    </div>

                    <ButtonPrimary class="w-fit flex items-center gap-2" to="/detail-blog">
                        <img src="../../assets/icons/home/heart.svg" alt="" />
                        Donate Now
                    </ButtonPrimary>
                </div>
            </div>
        </div>
    </div>
</template>