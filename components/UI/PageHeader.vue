<template>
  <header class="w-full h-[50vh] flex items-center justify-center relative px-2">
    <img class="absolute inset-0 w-full h-full object-cover" :src="props.imageUrl" alt="Imagem de fundo">

    <h1 class="text-4xl py-2 px-5 bg-gray-800 text-sky-400 font-mono uppercase font-bold text-center z-[1]">
      <slot></slot>
    </h1>
  </header>
</template>

<script setup lang="ts">
const props = defineProps<{
  imageUrl: string
}>()
</script>