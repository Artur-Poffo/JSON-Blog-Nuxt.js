<template>
  <section id="recent-posts" class="p-4">
    <SectionHeader>Recent posts</SectionHeader>

    <DefaultListItems>
      <li v-for="post in posts" :key="post.id">
        <PostResumeCard :post="post" />
      </li>
    </DefaultListItems>
  </section>
</template>

<script setup lang="ts">
import DefaultListItems from '~/components/UI/DefaultListItems.vue';
import PostResumeCard from '~/components/UI/PostResumeCard.vue';
import { type IPost } from '~/interfaces/IPost';
import SectionHeader from '../../components/UI/SectionHeader.vue';
import { useMyFetch } from '../../composables/useMyFetch';

const posts = ref<IPost[]>([])

async function fetchRecentPosts() {
  const { data: { value }, error } = await useMyFetch<IPost[]>('/posts?_sort=created_at&_order=desc&_limit=3');

  if (value && !error.value) {
    posts.value = value
    return;
  }

  throw new Error('Error fetching recent posts')
}

fetchRecentPosts()
</script>