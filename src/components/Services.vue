<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div
    class="flex flex-col gap-y-[60px] p-x-[170px] p-y-[60px] w-full h-fit justify-center justify-items-center items-center"
  >
    <div class="flex flex-col p-x-[10px] p-y-[20px] text-center justify-center">
      <h class="--font-poppins font-semibold text-[40px]">Our Services</h>
      <h class="font-Roboto font-regular text-[16px]"
        >Explore our range of premium service offerings.</h
      >
    </div>
    <div class="flex flex-row gap-x-[10px] w-fit justify-evenly">
      <ServiceOffering
        :planName="'Starter'"
        :price="'$80-$120'"
        :pages="'1-3 pages'"
        :attributes="[
          'Professional looking site',
          'Basic layout and mobile-friendly design',
          'Contact form',
          'Google Maps and business info',
          'Perfect for restaurants, salons, small shops',
        ]"
      />
      <ServiceOffering
        :planName="'Starter'"
        :price="'$80-$120'"
        :pages="'1-3 pages'"
        :attributes="[
          'Professional looking site',
          'Basic layout and mobile-friendly design',
          'Contact form',
          'Google Maps and business info',
          'Perfect for restaurants, salons, small shops',
        ]"
      />
      <ServiceOffering
        :planName="'Starter'"
        :price="'$80-$120'"
        :pages="'1-3 pages'"
        :attributes="[
          'Professional looking site',
          'Basic layout and mobile-friendly design',
          'Contact form',
          'Google Maps and business info',
          'Perfect for restaurants, salons, small shops',
        ]"
      />
    </div>
  </div>
</template>

<script setup lang="ts">
import ServiceOffering from './ServiceOffering.vue'
</script>
