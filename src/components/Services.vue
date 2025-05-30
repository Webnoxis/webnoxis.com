<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div
    class="flex flex-col gap-y-[60px] p-x-[170px] p-y-[60px] w-full h-fit justify-center justify-items-center items-center"
  >
    <div class="flex flex-col p-x-[10px] p-y-[20px] text-center justify-center">
      <h class="font-Poppins font-semibold text-[40px]">Our Services</h>
      <h class="font-Roboto font-regular text-[16px]"
        >Explore our range of premium service offerings.</h
      >
    </div>
    <div class="flex flex-row gap-x-[10px] w-fit justify-evenly">
      <ServiceOffering
        :planName="'Starter'"
        :price="'$100-$150'"
        :pages="'1-3 pages'"
        :attributes="[
          'Professional looking site',
          'Basic layout and mobile-friendly design',
          'Contact form',
          'Google Maps and business info',
          'Perfect for restaurants, salons, small shops',
        ]"
        class="first:rounded-l-[20px]"
      />
      <ServiceOffering
        :planName="'Standart'"
        :price="'$250-$300'"
        :pages="'3-5 pages'"
        :attributes="[
          'Custom design',
          'Basic SEO(Google search optimization)',
          'Simple photo gallery or menu ',
          'Basic blog or news section if needed',
        ]"
      />
      <ServiceOffering
        :planName="'Premium'"
        :price="'$550+'"
        :pages="'5-10 pages'"
        :attributes="['Advanced animations', 'Advanced and mobile-friendly design', 'Blog or portfolio section (optional)', '1 month of support and minor edits ']"
        class="last:rounded-r-[20px]"
      />
    </div>
    <RouterLink
      to="/contact"
      class="p-[12px] w-[240px] text-center items-center justify-center rounded-[10px] font-semibold text-white bg-[#713D86]  transition-all duration-300 ease-in-out hover:scale-105 hover:shadow-[0px_1px_12px_4px_rgba(0,_0,_0,_0.1)]"
    >
      Contact us
    </RouterLink>
  </div>
</template>

<script setup lang="ts">
import ServiceOffering from './ServiceOffering.vue'
</script>
