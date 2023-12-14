<template>
  <Navbar />
  <MobileMenu />

  <main class="min-h-screen bg-gray-300 text-zinc-800 scrollbar-thin scrollbar-thumb-sky-400 scrollbar-track-gray-900">
    <NuxtPage />
  </main>
</template>

<script setup lang="ts">
import MobileMenu from './components/Navigation/MobileMenu.vue';
import Navbar from './components/Navigation/Navbar.vue';
</script>