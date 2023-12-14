<template>
  <Navbar />

  <main class="min-h-screen bg-gray-300 text-zinc-800">
    <NuxtPage />
  </main>
</template>

<script setup lang="ts">
import Navbar from './components/Navigation/Navbar.vue';
</script>