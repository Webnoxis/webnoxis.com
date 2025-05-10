<script setup lang="ts">
  import Navbar from './components/Navbar.vue'
  import Footer from './components/Footer.vue'
  import { ref, onMounted, onUnmounted } from 'vue'

  const isScrolled = ref(false)

  const handleScroll = () => {
    isScrolled.value = window.scrollY > 50
  }

  onMounted(() => {
    window.addEventListener('scroll', handleScroll)
  })

  onUnmounted(() => {
    window.removeEventListener('scroll', handleScroll)
  })
</script>

<template>
  <header>
    <Navbar :class="[
      'transition-all duration-500 ease-in-out z-50',
      isScrolled ? 'bg-white shadow-md text-black' : 'bg-transparent text-white'
    ]"/>
  </header>

  <RouterView />

  <Footer />
</template>

<style scoped>
</style>
