<template>
  <NuxtLink v-if="props.to" :to="props.to">
    <button class="w-full py-2 px-4 rounded-sm bg-sky-400 text-gray-200 font-mono font-bold cursor-pointer">
      <slot></slot>
    </button>
  </NuxtLink>

  <button v-else class="w-full py-2 px-4 rounded-sm bg-sky-400 text-gray-200 font-mono font-bold cursor-pointer">
    <slot></slot>
  </button>
</template>

<script setup lang="ts">
const props = defineProps<{
  to?: string;
}>()
</script>