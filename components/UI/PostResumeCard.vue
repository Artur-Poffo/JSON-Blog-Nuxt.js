<template>
  <NuxtLink :to="`post/${post.id}`">
    <DefaultCard>
      <header class="flex flex-col">
        <img class="w-full min-h-[160px] object-cover rounded-md" :src="props.post.image_url"
          alt="Imagem de fundo do post">
        <h2 class="mt-2 text-2xl text-sky-400 font-mono font-bold">{{ props.post.title }}</h2>
        <span class="text-sm text-gray-500">Author: {{ props.post.author }}</span>
      </header>

      <main class="mt-3">
        <p>
          {{ props.post.description }}
        </p>
      </main>
    </DefaultCard>
  </NuxtLink>
</template>

<script setup lang="ts">
import { type IPost } from "../../interfaces/IPost";
import DefaultCard from './DefaultCard.vue';

const props = defineProps<{
  post: IPost
}>()
</script>