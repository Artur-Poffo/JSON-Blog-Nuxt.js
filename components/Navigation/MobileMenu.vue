<template>
  <button id="menu-button"
    class="w-8 h-8 bg-sky-400 rounded-full fixed flex items-center justify-center text-center top-5 right-5 z-[999]"
    @click="toggle">+</button>

  <Menu class="fixed top-16 right-5 max-w-sm p-3 bg-gray-400 rounded-md" :model="items" :popup="popup"
    :unstyled="false" />
</template>

<script setup lang="ts">
import Menu from 'primevue/menu';

const items: {
  label: string
}[] = [
    {
      label: "Item 1"
    },
    {
      label: "Item 2"
    },
    {
      label: "Item 3"
    },
  ]

const popup = ref(true)

function toggle() {
  popup.value = !popup.value
}
</script>