<template>
  <HomeSection />
  <RecentPostsSection />
</template>

<script setup lang="ts">
import HomeSection from "../sections/Home/HomeSection.vue";
import RecentPostsSection from "../sections/Home/RecentPostsSection.vue";

useSeoMeta({
  title: "JSON Blog",
  description: "Fake JSON Blog to study Nuxt.js",
})
</script>