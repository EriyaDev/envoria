<script setup>
import { ref, nextTick, watch } from 'vue'
import iconPlus from '../../../assets/icons/home/plus.svg'
import iconMinus from '../../../assets/icons/home/minus.svg'

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
    title: 'What is Envoria waste transportation? ',
    content:
      'Envoria is a smart waste transport platform that connects businesses and households with efficient, eco-friendly collection and recycling routes. We handle everything from pickup to final disposal.',
  },
  {
    title: 'How does Envoria reduce environmental impact? ',
    content:
      'We use low-emission vehicles, AI-optimized routes, and green recycling partnerships to significantly cut carbon output. Every shipment is tracked and reported for full environmental transparency.',
  },
  {
    title: 'Do you offer customized waste collection plans? ',
    content:
      "Yes. Whether you're a small business or a large industrial facility, we tailor collection schedules, vehicle types, and routes to match your exact waste volume and location needs.",
  },
  {
    title: 'What areas does Envoria currently serve?',
    content:
      "Envoria currently operates across major urban and industrial zones globally. We're continuously expanding our network — reach out to check if your area is covered.",
  },
  {
    title: 'Can Envoria handle large-scale industrial waste?',
    content:
      'Absolutely. Our fleet is equipped to manage high-volume industrial waste across multiple sites. We ensure full compliance with local environmental regulations throughout the process.',
  },
]
</script>

<template>
  <div class="bg-card-color">
    <div class="section-container py-10 lg:py-14">
      <div class="flex flex-col gap-3 items-center">
        <span
          class="flex flex-row items-center w-fit px-3 py-1 bg-black/5 text-text-text-primary-color border border-border-color/55 text-small rounded-full font-semibold"
        >
          <div class="w-2 h-2 bg-accent-color rounded-full mr-2 animate-pulse"></div>
          FAQS</span
        >
        <h2
          class="text-display font-medium text-text-text-primary-color mt-10 text-center max-w-[90%] md:max-w-[70%] xl:max-w-[60%]"
        >
          Clearing <span class="text-text-primary-color/55">doubts</span> about our
          <span class="text-text-primary-color/55">waste</span> transport services
        </h2>
      </div>
      <div class="w-full lg:max-w-[85%] mx-auto mt-10">
        <div class="flex flex-col gap-5">
          <div v-for="(item, index) in faqs" :key="index" class="flex flex-col">
            <!-- Header -->
            <div
              data-aos="fade-up"
              :data-aos-delay="index + '00'"
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
  </div>
</template>
