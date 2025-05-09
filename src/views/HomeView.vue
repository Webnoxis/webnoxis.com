<script setup lang="ts">
  import WelcomeItem from "../components/WelcomeItem.vue"
  import Services from "../components/Services.vue"
  import About from "../components/About.vue"
  import Partners from "../components/Partners.vue"
</script>

<template>
  <main class="flex flex-col gap-y-[60px]">
    <WelcomeItem />
    <Services />
    <About />
    <Partners />
  </main>
</template>
