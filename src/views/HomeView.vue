<script setup lang="ts">
import { ref } from 'vue'
import WelcomeItem from "../components/WelcomeItem.vue"
import Services from "../components/Services.vue"
import About from "../components/About.vue"
import Partners from "../components/Partners.vue"
import Contact from "../components/Contact.vue"

// Define the refs with proper types
const aboutRef = ref<InstanceType<typeof About> | null>(null)
const servicesRef = ref<InstanceType<typeof Services> | null>(null)

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
    <Contact />
  </main>
</template>
