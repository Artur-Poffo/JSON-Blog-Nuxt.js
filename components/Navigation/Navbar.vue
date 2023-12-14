<template>
  <header class="hidden fixed top-0 w-full py-2 px-5 md:flex items-center justify-evenly bg-gray-900 z-[999]">
    <NuxtLink to="/">
      <h1 class="text-3xl text-sky-400 font-mono font-bold">JSON Blog</h1>
    </NuxtLink>

    <nav class="flex gap-5">
      <ul class="flex gap-4">
        <li>
          <NavLink to="/">Home</NavLink>
        </li>
        <li>
          <NavLink to="/posts">All posts</NavLink>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script setup lang="ts">
import NavLink from './NavLink.vue';
</script>