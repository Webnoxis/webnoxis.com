<template>
  <div     ref="animatedElement" :class="['flex flex-col gap-y-[10px] w-[300px] items-left h-[280px] border-[rgba(0,0,0,0.1)] border rounded-[10px] p-[12px] transition-all duration-400 ease-in-out', isVisible ? 'animate-zoom-in' : 'opacity-0 scale-0']">
    <div class="flex flex-col gap-y-[4px] self-start text-left font-Roboto">
      <h class="font-Roboto font-medium text-[20px]">{{ planName }}</h>
      <h class="font-['Roboto', sans-serif] font-regular text-[16px]">{{ price }}</h>
      <h class="font-Roboto font-regular text-[12px] text-[#6E6E6E]">{{ pages }}</h>
    </div>
    <div class="flex flex-col gap-y-[10px]">
      <ServiceAttribute v-for="(attr, index) in attributes" :key="index" :attribute="attr" />
    </div>
  </div>
</template>

<script setup lang="ts">
import ServiceAttribute from './ServiceAttribute.vue'

// eslint-disable-next-line @typescript-eslint/no-unused-vars
const props = defineProps<{
  planName: string
  price: string
  pages: string
  attributes: string[]
}>()


import { ref, onMounted, onUnmounted } from 'vue'

const isVisible = ref(false)
const animatedElement = ref(null)

const onIntersect = (entries, observer) => {
  if (entries[0].isIntersecting) {
    isVisible.value = true
    observer.disconnect() // Only animate once
  }
}

onMounted(() => {
  const observer = new IntersectionObserver(onIntersect, {
    threshold: 0.5
  })
  if (animatedElement.value) {
    observer.observe(animatedElement.value)
  }
})


</script>

<style scoped>
@keyframes zoomInOnce {
  0% {
    opacity: 0;
    transform: scale(0);
  }
  100% {
    opacity: 1;
    transform: scale(1);
  }
}

.animate-zoom-in {
  animation: zoomInOnce 0.7s ease-out forwards;
}
</style>
