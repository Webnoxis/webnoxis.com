<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div class="fixed flex flex-row w-full h-[4rem] p-[1.3rem] justify-between">
    <div class="flex flex-row items-center justify-items-start">
      <RouterLink to="/" class="font-Poppins font-semibold text-[1.5rem]">Webnoxis</RouterLink>
    </div>
    <div class="flex flex-row items-center justify-items-end gap-x-5 text-[1.1rem] font-Roboto">
      <RouterLink class="group relative" to="/">
        Home
          <span
            class="absolute left-0 bottom-0 h-[2px] w-0 bg-[#713D86] transition-all duration-300 group-hover:w-full"
          ></span>
      </RouterLink>
      <RouterLink class="group relative" to="/services">
        Services
        <span
            class="absolute left-0 bottom-0 h-[2px] w-0 bg-[#713D86] transition-all duration-300 group-hover:w-full"
        ></span>
      </RouterLink>
      <RouterLink class="group relative" to="/about">
        About
        <span
            class="absolute left-0 bottom-0 h-[2px] w-0 bg-[#713D86] transition-all duration-300 group-hover:w-full"
        ></span>
      </RouterLink>
      <RouterLink class="group relative" to="/contact">
        Contact
        <span
            class="absolute left-0 bottom-0 h-[2px] w-0 bg-[#713D86] transition-all duration-300 group-hover:w-full"
        ></span>
      </RouterLink>
    </div>
  </div>
</template>
