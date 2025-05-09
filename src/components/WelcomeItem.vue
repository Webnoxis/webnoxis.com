<template>
  <div class="flex flex-row w-full h-fit justify-center">
    <div class="flex flex-col items-center justify-center w-fit h-fit text-center gap-y-[0.5rem]">
      <h class="font-Poppins text-[2.5rem] font-semibold">Welcome to Webnoxis</h>
      <h class="font-Roboto text-[1rem] font-regular"
        >Your one-stop destination for top-notch services.</h
      >
      <div class="font-Roboto flex flex-row gap-x-[12px]">
        <span
          class="p-[12px] w-[240px] text-center items-center justify-center rounded-[10px] border border-black font-semibold"
          @click="$emit('scrollToAbout')"
        >
          Learn More
        </span>
        <span
          class="p-[12px] w-[240px] text-center items-center justify-center rounded-[10px] font-semibold text-white bg-[#713D86]"
          @click="$emit('scrollToServices')"
        >
          Get Started
        </span>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts"></script>
