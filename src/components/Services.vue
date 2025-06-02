<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div
    class="flex flex-col gap-y-[60px] p-x-[170px] p-y-[60px] w-full h-fit justify-center justify-items-center items-center"
  >
    <div class="flex flex-col p-x-[10px] p-y-[20px] text-center justify-center max-xl:max-w-[300px]">
      <h class="font-Poppins font-semibold text-[40px]">Our Services</h>
      <h class="font-Roboto font-regular text-[16px]"
        >Explore our range of premium service offerings.</h
      >
    </div>
    <div class="flex flex-row gap-x-[10px] w-fit justify-evenly max-xl:flex-col max-xl:items-center max-xl:gap-y-[10px]">
      <ServiceOffering
        :planName="'Starter'"
        :price="'$200-$300'"
        :pages="'1-3 pages'"
        :attributes="[
          'Professional looking site',
          'Basic layout and mobile-friendly design',
          'Contact form',
          'Google Maps and business info',
          'Perfect for restaurants, salons, small shops',
          'Fast loading & optimized images',
        ]"
        class="xl:first:rounded-l-[20px]"
      />
      <ServiceOffering
        :planName="'Standart'"
        :price="'$450-$600'"
        :pages="'4-6 pages'"
        :attributes="[
          'Custom design',
          'Basic SEO(Google search optimization)',
          'Simple photo gallery or menu ',
          'Basic blog or news section if needed',
          'Social media integration (buttons, feeds)',
        ]"
      />
      <ServiceOffering
        :planName="'Premium'"
        :price="'$900+'"
        :pages="'7-12 pages'"
        :attributes="['Advanced animations', 'Advanced and mobile-friendly design', 'Blog or portfolio section (optional)', '3 rounds of revisions + 2 months of post-launch support', 'CMS integration for easy content management' ]"
        class="xl:last:rounded-r-[20px]"
      />
    </div>
    <span
      @click="$emit('scrollToContact')"
      class="p-[12px] w-[240px] text-center items-center justify-center rounded-[10px] font-semibold text-white bg-[#713D86]  transition-all duration-300 ease-in-out hover:scale-105 hover:shadow-[0px_1px_12px_4px_rgba(0,_0,_0,_0.1)]"
    >
      Contact us
  </span>
  </div>
</template>

<script setup lang="ts">
import ServiceOffering from './ServiceOffering.vue'
</script>
