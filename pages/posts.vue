<template>
  <PageHeader
    imageUrl="https://images.unsplash.com/photo-1432821596592-e2c18b78144f?q=80&w=1000&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8NHx8YmxvZ3xlbnwwfHwwfHx8MA%3D%3D">
    All posts
  </PageHeader>

  <section id="list-posts" class="py-10 px-4">
    <DefaultListItems>
      <li v-for="post in posts" :key="post.id">
        <PostResumeCard :post="post" />
      </li>
    </DefaultListItems>
  </section>
</template>

<script setup lang="ts">
import DefaultListItems from '~/components/UI/DefaultListItems.vue';
import PageHeader from '~/components/UI/PageHeader.vue';
import PostResumeCard from '~/components/UI/PostResumeCard.vue';
import { type IPost } from '~/interfaces/IPost';
import { useMyFetch } from '../composables/useMyFetch';

const posts = ref<IPost[]>([])

async function fetchRecentPosts() {
  const { data: { value }, error } = await useMyFetch<IPost[]>('/posts?_sort=created_at&_order=desc');

  if (value && !error.value) {
    posts.value = value
    return;
  }

  throw new Error('Error fetching recent posts')
}

fetchRecentPosts()
</script>