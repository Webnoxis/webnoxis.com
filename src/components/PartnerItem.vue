<template>
 <span class="flex flex-col
 gap-y-[10px] py-[10px]
 px-[30px] items-center
 border-[1px] border-[rgba(0,0,0,0.1)]
 rounded-[5px] w-[220px] h-[150px] transition-all duration-300 ease-in-out
 shadow-[7px_7px_6px_0px_rgba(0,_0,_0,_0.3)]
 group hover:shadow-[13px_13px_6px_0px_rgba(0,_0,_0,_0.2)]
 hover:scale-110
" @click="redirect">
    <img class="w-[100px] group-hover:w-[70px] group-hover: transition-all duration-300 ease-in-out" :src="companyLogoUrl" :alt="companyName" />
    <h class="font-Poppins text-[20px] opacity-0 group-hover:opacity-100 transition-all duration-300 ease-in-out">{{ companyName }}</h>
 </span>
</template>

<script setup lang="ts">
const props = defineProps<{
  companyName: string,
  companyIcon: string,
  url: string
}>()

function redirect() {
    window.open(props.url, '_blank')
}

const companyLogoUrl = new URL(`../assets/${props.companyIcon}`, import.meta.url).href
</script>
