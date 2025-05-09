<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div
    class="flex flex-col gap-y-[60px] p-x-[170px] p-y-[60px] w-full h-fit justify-center justify-items-center items-center"
  >
    <div class="flex flex-col p-x-[10px] p-y-[20px] text-center justify-center">
      <h class="font-Poppins font-semibold text-[40px]">Partners</h>
    </div>
    <div class="flex flex-row gap-x-[20px] w-fit justify-evenly">
      <PartnerItem :companyName="'QuackStack Ltd'" :companyIcon="'quackstack.svg'"/>
      <PartnerItem :companyName="'QuackStack Ltd'" :companyIcon="'quackstack.svg'"/>
      <PartnerItem :companyName="'QuackStack Ltd'" :companyIcon="'quackstack.svg'"/>
      <PartnerItem :companyName="'QuackStack Ltd'" :companyIcon="'quackstack.svg'"/>

    </div>
  </div>
</template>

<script setup lang="ts">
  import PartnerItem from "./PartnerItem.vue"
</script>
