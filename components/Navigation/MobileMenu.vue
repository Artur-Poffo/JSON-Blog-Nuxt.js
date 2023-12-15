<template>
  <button id="menu-button"
    class="w-8 h-8 bg-sky-400 rounded-full fixed flex md:hidden items-center justify-center text-center top-5 right-5 z-[999]"
    @click="toggle">
    <Bars3Icon class="w-5 h-5" />
  </button>

  <Menu class="fixed top-16 right-5 max-w-sm p-3 bg-gray-800 rounded-md z-[999]" :model="items" :popup="popup" :unstyled="false">
    <template #item="{item, props, label}" >
      <NuxtLink class="text-gray-200 bg-transparent p-2 rounded-md hover:bg-gray-700" :to="item.url" >
        {{ label }}
      </NuxtLink>
    </template>
  </Menu>
</template>

<script setup lang="ts">
import Menu from 'primevue/menu';
import { Bars3Icon } from "@heroicons/vue/24/solid"

const items: {
  label: string,
  url: string
}[] = [
    {
      label: "Home",
      url: "/"
    },
    {
      label: "All posts",
      url: "/posts"
    },
  ]

const popup = ref(true)

function toggle() {
  popup.value = !popup.value
}
</script>