<script setup lang="ts">
  import Navbar from './components/Navbar.vue'
  import Footer from './components/Footer.vue'
  import { ref, onMounted, onUnmounted } from 'vue'
  import type { ComponentPublicInstance } from 'vue'

  const isScrolled = ref(false)

  const pageRef = ref<ComponentPublicInstance<HomeComponentExposed> | null>(null)

  type HomeComponentExposed = {
    aboutRef: ComponentPublicInstance | null
    servicesRef: ComponentPublicInstance | null
    contactRef: ComponentPublicInstance | null
  }

  const handleScroll = () => {
    isScrolled.value = window.scrollY > 50
  }

  onMounted(() => {
    window.addEventListener('scroll', handleScroll)
  })

  onUnmounted(() => {
    window.removeEventListener('scroll', handleScroll)
  })

  function scrollToAbout() {
    pageRef.value?.aboutRef?.$el?.scrollIntoView({ behavior: 'smooth' })
  }

  function scrollToServices() {
    pageRef.value?.servicesRef?.$el?.scrollIntoView({ behavior: 'smooth' })
  }

  function scrollToContact() {
    pageRef.value?.contactRef?.$el?.scrollIntoView({ behavior: 'smooth' })
  }
</script>

<template>
  <header>
    <Navbar :class="[
      'transition-all duration-500 ease-in-out z-50 max-xl:bg-transparent max-xl:text-white max-xl:shadow-none max-xl:invisible',
      isScrolled ? 'bg-white shadow-md text-black' : 'bg-transparent text-white'
    ]"
    @scrollToAbout="scrollToAbout"
    @scrollToServices="scrollToServices"
    @scrollToContact="scrollToContact"/>
  </header>

  <RouterView v-slot="{ Component: RouteComponent }">
        <component :is="RouteComponent" ref="pageRef" />
  </RouterView>

  <Footer class="mt-[60px]"/>
</template>

<style scoped>
</style>
