<template>
  <section id="home" class="min-h-screen flex flex-col lg:flex-row items-center justify-evenly px-4">
    <div class="max-w-xl flex flex-col gap-2">
      <h1 class="text-5xl font-mono font-bold">Hello, this is a fake blog to study Nuxt.js ;)</h1>
      <p>I'm studying about some concepts of Nuxt.js and this is a simple blog to practice. The posts are saved on a JSON
        file using json-server lib</p>
      <DefaultButton to="/#recent-posts">View recent posts</DefaultButton>
    </div>

    <img src="/images/nuxt-logo.png" alt="Logo do Nuxt.js">
  </section>
</template>

<script setup lang="ts">
import DefaultButton from "../../components/UI/DefaultButton.vue";
</script>