<script setup>
import ButtonPrimary from '../micro/ButtonPrimary.vue'
import ButtonSecondary from '../micro/ButtonSecondary.vue'
</script>

<template>
    <div class="bg-[#f5f5f5] py-10">
        <div class="section-container mx-auto">
            <div class="w-full rounded-xl relative overflow-hidden h-64 md:h-80 lg:h-100 xl:h-150">

                <!-- ░░ VIDEO BACKGROUND ░░ -->
                <video class="absolute inset-0 w-full h-full object-cover" autoplay loop muted playsinline
                    poster="../../assets/images/backup.png">
                    <source src="../../assets/videos/home.mp4" type="video/mp4" />
                </video>

                <!-- ░░ OVERLAY — gradien gelap tipis di sisi kiri agar teks terbaca ░░ -->
                <div class="absolute inset-0"
                    style="background: linear-gradient(to right, rgba(0,0,0,0.52) 0%, rgba(0,0,0,0.18) 55%, rgba(0,0,0,0) 100%);">
                </div>

                <!-- ░░ TEKS MENGAMBANG — pojok kiri, vertikal tengah ░░ -->
                <div class="absolute inset-0 flex items-start z-10 p-5 md:p-18">
                    <div class="border-l-4 border-accent-color pl-2 md:pl-4">
                        <p class="text-white font-medium font-family-inter leading-snug text-sm md:text-2xl text-enter">
                            Track your waste from collection to recycling –
                        </p>
                        <p
                            class="text-white font-medium font-family-inter leading-snug text-sm md:text-2xl text-enter-delay">
                            See how simple it can be
                        </p>
                    </div>
                </div>

            </div>
        </div>
    </div>
</template>