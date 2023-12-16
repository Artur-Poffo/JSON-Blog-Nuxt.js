<template>
  <article
    v-if="post"
    class="w-full max-w-screen-lg mx-auto pt-32 px-4 pb-10 flex flex-col gap-12"
  >
    <header class="flex flex-col gap-2">
      <img
        class="w-full rounded-md"
        :src="post.image_url"
        alt="Imagem do post"
      />

      <div class="mt-4">
        <h1 class="text-4xl font-mono font-bold text-sky-400">
          {{ post.title }}
        </h1>
        <span class="text-sm font-bold text-gray-500">{{ post.author }}</span>
      </div>

      <ul class="flex flex-wrap items-center gap-2">
        <li v-for="tag in post.tags" :key="tag">
          <TagComponent>
            {{ tag }}
          </TagComponent>
        </li>
      </ul>
    </header>

    <main
      v-html="formattedContent"
      class="prose max-w-none break-words prose-h1:text-sky-400 prose-h1:text-3xl prose-h1:font-mono prose-h1:font-bold prose-img:rounded-md prose-a:underline prose-a:underline-offset-4 prose-a:decoration-sky-400 prose-a:transition-colors prose-a:font-normal hover:prose-a:text-sky-400"
    ></main>
  </article>
</template>

<script setup lang="ts">
import TagComponent from "@/components/UI/TagComponent.vue";
import { type IPost } from "@/interfaces/IPost";
import { micromark } from "micromark";

const route = useRoute();
const router = useRouter();

const post = ref<IPost | null>(null);
const formattedContent = ref("");

async function getPostDetails() {
  const {
    data: { value },
    error,
  } = await useMyFetch<IPost>(`/posts/${route.params.id}`);

  if (value && !error.value) {
    return value;
  }

  router.replace("/");
  throw new Error("Error on fetch post details");
}

getPostDetails()
  .then((postData) => {
    if (!postData) {
      router.push("/");
    }

    useSeoMeta({
      title: `JSON Blog | ${postData.title}`,
      description: () => `${postData.description}`,
    });

    post.value = postData;
    formattedContent.value = micromark(post.value.content);
  })
  .catch((err) => console.error(err));
</script>

