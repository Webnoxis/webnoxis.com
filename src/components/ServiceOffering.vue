<template>
  <div class="flex flex-col gap-y-[10px] w-[300px] items-left h-[280px] border-[rgba(0,0,0,0.1)] border rounded-[10px] p-[12px]">
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
</script>
