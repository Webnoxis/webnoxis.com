<template>
  <div class="flex flex-col gap-y-[0px] w-[520px] h-[60px]">
    <h class="font-Roboto font-semibold text-[14px]">{{ FieldName }}</h>
    <input class="outline-none border-1 border-[rgba(0,0,0,0.1)] rounded-[5px] w-full h-[35px] p-2 font-Roboto" :placeholder="placeholder">
  </div>
</template>

<script setup lang="ts">
const props = defineProps<{
  FieldName: string,
  placeholder: string
}>()
</script>