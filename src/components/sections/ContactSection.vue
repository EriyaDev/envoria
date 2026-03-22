<script setup>
import ButtonPrimary from '../micro/ButtonPrimary.vue'
import ButtonSecondary from '../micro/ButtonSecondary.vue'
</script>

<template>
    <div class="bg-[#f5f5f5] py-10">
        <div class="section-container grid grid-cols-2 gap-5 mx-auto">
            <div class="flex flex-col gap-3 items-start">
                <span
                    class="flex flex-row items-center w-fit px-3 py-1 bg-black/5 text-text-primary-color border border-[#2D612B]/13 text-small rounded-full font-semibold">
                    <div class="w-2 h-2 bg-accent-color rounded-full mr-2"></div>
                    Get In Touch
                </span>

                <div class="flex flex-col gap-4">
                    <h2 class="medium-heading font-medium text-text-primary-color mt-10 text-start">
                        Who can <span class="text-text-primary-color/55">partner</span> <br>
                        with us?
                    </h2>
                    <p class="text-body font-medium max-w-[70%] text-[#464646]">We strive to make our waste
                        transport process
                        simple and
                        accessible to every business.</p>

                    <div class="flex flex-col gap-2">
                        <div class="flex flex-col">
                            <div class="flex items-center justify-between w-full p-4 rounded-xl bg-primary-color">
                                <p class="text-body font-medium">Waste volume requirements</p>
                                <img src="../../assets/icons/home/plus.svg" alt="">
                            </div>

                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>