<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div class="fixed flex flex-row w-full h-[4rem] p-[1.3rem] justify-between max-xl:flex-col max-xl:items-center max-xl:justify-center max-xl:absolute">
    <div class="flex flex-row items-center justify-items-start">
      <RouterLink to="/" class="font-Poppins font-semibold text-[1.5rem]">Webnoxis</RouterLink>
    </div>
    <div class="flex flex-row items-center justify-items-end gap-x-5 text-[1.1rem] font-Roboto max-xl:justify-center">
      <!-- <RouterLink class="group relative" to="/">
        Home
          <span
            class="absolute left-0 bottom-0 h-[2px] w-0 bg-[#713D86] transition-all duration-300 group-hover:w-full"
          ></span>
      </RouterLink> -->
      <span  class="group relative cursor-pointer" @click="$emit('scrollToServices')">
        Services
        <span
            class="absolute left-0 bottom-0 h-[2px] w-0 bg-[#713D86] transition-all duration-300 group-hover:w-full"
        ></span>
      </span>
      <span class="group relative cursor-pointer" @click="$emit('scrollToAbout')">
        About
        <span
            class="absolute left-0 bottom-0 h-[2px] w-0 bg-[#713D86] transition-all duration-300 group-hover:w-full"
        ></span>
      </span>
      <span class="group relative cursor-pointer" @click="$emit('scrollToContact')">
        Contact
        <span
            class="absolute left-0 bottom-0 h-[2px] w-0 bg-[#713D86] transition-all duration-300 group-hover:w-full"
        ></span>
      </span>
    </div>
  </div>
</template>
