<script setup>
import { ref, nextTick, watch } from 'vue'
import iconPlus from '../../assets/icons/home/plus.svg'
import iconMinus from '../../assets/icons/home/minus.svg'

const openIndex = ref(null)
const contentHeights = ref({})
const contentRefs = ref({})

const setRef = (el, index) => {
  if (el) contentRefs.value[index] = el
}

const toggle = async (index) => {
  openIndex.value = openIndex.value === index ? null : index
  await nextTick()
  if (contentRefs.value[index]) {
    contentHeights.value[index] = contentRefs.value[index].scrollHeight
  }
}

const faqs = [
  {
    title: 'Waste volume requirements',
    content:
      "We accept partners generating a minimum of 500kg of waste per month. Whether you're a small business or a large industrial facility, our fleet scales to match your output.",
  },
  {
    title: 'Business type & industry',
    content:
      'We work with manufacturing plants, construction firms, hospitality businesses, healthcare facilities, and more. If your operations generate waste, we have a solution tailored for you.',
  },
  {
    title: 'Location & service area',
    content:
      "Our network currently covers major urban and industrial zones. We're continuously expanding — reach out to check if your area is within our active service routes.",
  },
  {
    title: 'Compliance & permits',
    content:
      'Partners are required to hold valid waste disposal documentation as per local environmental regulations. Our team can guide you through the compliance process if needed.',
  },
]
</script>

<template>
  <div class="bg-[#f5f5f5] py-10">
    <div class="section-container grid grid-cols-1 xl:grid-cols-2 gap-20 mx-auto">
      <div class="flex flex-col gap-3 items-start">
        <span
          class="flex flex-row items-center w-fit px-3 py-1 bg-black/5 text-text-primary-color border border-[#2D612B]/13 text-small rounded-full font-semibold"
        >
          <div class="w-2 h-2 bg-accent-color rounded-full mr-2"></div>
          Get In Touch
        </span>

        <div class="flex flex-col gap-4">
          <h2
            data-aos="fade-right"
            data-aos-delay="00"
            class="medium-heading font-medium text-text-primary-color mt-10 text-start"
          >
            Who can <span class="text-text-primary-color/55">partner</span> <br />
            with us?
          </h2>
          <p
            data-aos="fade-right"
            data-aos-delay="200"
            class="text-body font-medium xl:max-w-[70%] text-[#464646]"
          >
            We strive to make our waste transport process simple and accessible to every business.
          </p>

          <div class="flex flex-col gap-5">
            <div v-for="(item, index) in faqs" :key="index" class="flex flex-col">
              <!-- Header -->
              <div
                data-aos="fade-up"
                data-aos-delay="00"
                class="flex items-center justify-between w-full p-7.5 bg-primary-color cursor-pointer select-none transition-all duration-300"
                :class="openIndex === index ? 'rounded-t-xl' : 'rounded-xl'"
                @click="toggle(index)"
              >
                <p class="text-body font-medium">{{ item.title }}</p>
                <img
                  :src="openIndex === index ? iconMinus : iconPlus"
                  alt=""
                  class="transition-all duration-300"
                />
              </div>

              <!-- Content -->
              <div
                class="overflow-hidden transition-all duration-300 ease-in-out"
                :style="
                  openIndex === index
                    ? `max-height: ${contentHeights[index] ?? 200}px; opacity: 1`
                    : 'max-height: 0px; opacity: 0'
                "
              >
                <div
                  :ref="(el) => setRef(el, index)"
                  class="p-7.5 pt-0 rounded-b-xl bg-primary-color"
                >
                  <p class="text-small font-medium text-text-third-color">
                    {{ item.content }}
                  </p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="flex flex-col gap-5 xl:mt-13">
        <img src="../../assets/images/contact/image-1.png" alt="" />

        <div class="flex flex-col gap-4">
          <h3 class="small-heading font-medium">Documents required:</h3>

          <ul class="grid grid-cols-1 md:grid-cols-2 w-fit h-fit gap-y-6">
            <li class="flex items-center gap-2">
              <img src="../../assets/icons/home/checkmark-green.svg" alt="" />
              <span class="text-body font-medium text-text-third-color"
                >Waste disposal license</span
              >
            </li>
            <li class="flex items-center gap-2">
              <img src="../../assets/icons/home/checkmark-green.svg" alt="" />
              <span class="text-body font-medium text-text-third-color"
                >Proof of business registration</span
              >
            </li>
            <li class="flex items-center gap-2">
              <img src="../../assets/icons/home/checkmark-green.svg" alt="" />
              <span class="text-body font-medium text-text-third-color">Site location details</span>
            </li>
            <li class="flex items-center gap-2">
              <img src="../../assets/icons/home/checkmark-green.svg" alt="" />
              <span class="text-body font-medium text-text-third-color"
                >Environmental compliance cert</span
              >
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>
