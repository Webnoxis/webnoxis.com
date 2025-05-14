<template>
  <div class="flex flex-row w-full h-[1000px] justify-center items-center bg-radial-[at_20%_25%] from-white to-zinc-600 to-95% backdrop-blur-md">
    <div class="flex flex-col items-center justify-center w-fit h-fit text-center gap-y-[0.5rem] mb-[200px]">
      <h class="font-Poppins text-[2.5rem] font-semibold">Welcome to Webnoxis</h>
      <h class="font-Roboto text-[1rem] font-regular"
        >Your one-stop destination for top-notch services.</h
      >
      <div class="font-Roboto flex flex-row gap-x-[12px]">
        <!-- <span
          class="p-[12px] w-[240px] text-center items-center justify-center rounded-[10px] border border-black font-semibold transition-all duration-300 ease-in-out hover:scale-105 hover:shadow-[0px_1px_12px_4px_rgba(0,_0,_0,_0.1)]"
          @click="$emit('scrollToAbout')"
        >
          Learn More
        </span> -->
        <span
          class="cursor-pointer p-[12px] w-[240px] text-center items-center justify-center rounded-[10px] font-semibold text-white bg-[#713D86] transition-all duration-300 ease-in-out hover:scale-105 hover:shadow-[0px_1px_12px_4px_rgba(0,_0,_0,_0.1)]
"
          @click="$emit('scrollToServices')"
        >
          Get Started
        </span>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts"></script>
