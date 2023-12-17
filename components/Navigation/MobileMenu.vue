<template>
  <button id="menu-button"
    class="w-8 h-8 bg-sky-400 rounded-full fixed flex md:hidden items-center justify-center text-center top-5 right-5 z-[999]"
    @click="toggle">
    <Icon name="material-symbols:menu" color="black" />
  </button>

  <Menu class="fixed top-16 right-5 max-w-sm p-3 bg-gray-800 rounded-md z-[999]" :model="items" :popup="popup"
    :unstyled="false">
    <template #item="{ item, props, label }">
      <NuxtLink @click="toggle" class="text-gray-200 my-12 rounded-md hover:text-gray-100" :to="item.url">
        {{ label }}
      </NuxtLink>
    </template>
  </Menu>
</template>

<script setup lang="ts">
import Menu from 'primevue/menu';

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