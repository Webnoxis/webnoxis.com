<template>
  <span class="flex flex-row gap-x-[10px] items-center w-full h-fit">
    <div class="w-[10px] h-[10px] bg-[#838383] rounded-[10px]"></div>
    <p class="font-Roboto text-[12px]">{{ attribute }}</p>
  </span>
</template>

<script setup lang="ts">
// eslint-disable-next-line @typescript-eslint/no-unused-vars
const props = defineProps<{
  attribute: string
}>()
</script>
