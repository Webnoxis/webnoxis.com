<script setup lang="ts">
  import WelcomeItem from "../components/WelcomeItem.vue"
  import Services from "../components/Services.vue"
  import About from "../components/About.vue"
  import Partners from "../components/Partners.vue"
  import { ref } from 'vue'

const aboutRef = ref(null)
const servicesRef = ref(null)

function scrollToAbout() {
  aboutRef.value?.$el?.scrollIntoView({ behavior: 'smooth' })
}

function scrollToServices() {
  servicesRef.value?.$el?.scrollIntoView({ behavior: 'smooth' })
}
</script>

<template>
  <main class="flex flex-col gap-y-[60px] ">
    <WelcomeItem
      @scrollToAbout="scrollToAbout"
      @scrollToServices="scrollToServices"/>
    <Services ref="servicesRef"/>
    <About ref="aboutRef"/>
    <Partners />
  </main>
</template>
