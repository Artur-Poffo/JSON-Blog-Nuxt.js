<template>
  <NuxtLink :to="props.to"
    class="opacity-80 text-gray-200 inline-block py-px px-2 bg-transparent rounded-sm transition-all hover:bg-gray-800 hover:opacity-100">
    <slot></slot>
  </NuxtLink>
</template>

<script setup lang="ts">
const props = defineProps<{
  to: string
}>()

const route = useRoute()
const isActive = ref(false)

if (route.path === props.to) {
  isActive.value = true
} else {
  isActive.value = false
}
</script>

<style scoped>
.router-link-active {
  @apply opacity-100 bg-gray-800
}
</style>