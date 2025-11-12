<template>
  <UContainer>
    <UPageHeader
      title="S0FTS0RR0W's Blog"
      description="Thoughts, stories and ideas from the world of a software developer."
      class="py-12"
    />

    <div class="flex justify-center mb-12">
      <UInput
        v-model="searchQuery"
        icon="i-heroicons-magnifying-glass"
        size="lg"
        color="white"
        :trailing="false"
        placeholder="Search articles..."
        class="w-full max-w-md"
      />
    </div>

    <UPageGrid>
      <UCard v-for="post in filteredPosts" :key="post.id">
        <template #header>
          <h2 class="text-xl font-bold text-primary">{{ post.title }}</h2>
        </template>

        <p class="text-gray-500 dark:text-gray-400">{{ post.excerpt }}</p>

        <template #footer>
          <div class="flex justify-between items-center">
            <span class="text-sm text-gray-400 dark:text-gray-500">{{ post.date }}</span>
            <UButton :to="`/blog/${post.slug}`" variant="link">Read More</UButton>
          </div>
        </template>
      </UCard>
    </UPageGrid>
  </UContainer>
</template>

<script setup>
import { ref, computed } from 'vue';

const searchQuery = ref('');

const posts = ref([
  {
    id: 1,
    title: 'The Art of Debugging',
    excerpt: 'Debugging is like being a detective in a crime movie where you are also the murderer. This post explores effective debugging strategies.',
    date: 'Oct 26, 2025',
    slug: 'art-of-debugging'
  },
  {
    id: 2,
    title: 'A Deep Dive into Vue 3 Composables',
    excerpt: 'Vue 3\'s Composition API introduces a powerful way to write and reuse logic. Let\'s explore how to create our own composables.',
    date: 'Oct 22, 2025',
    slug: 'vue-3-composables'
  },
  {
    id: 3,
    title: 'Why I Chose Nuxt.js for my Blog',
    excerpt: 'Nuxt.js offers a great developer experience and performance. Here are the reasons why I decided to build my blog with it.',
    date: 'Oct 18, 2025',
    slug: 'why-nuxt-js'
  },
]);

const filteredPosts = computed(() => {
  if (!searchQuery.value) {
    return posts.value;
  }
  return posts.value.filter(post =>
    post.title.toLowerCase().includes(searchQuery.value.toLowerCase()) ||
    post.excerpt.toLowerCase().includes(searchQuery.value.toLowerCase())
  );
});
</script>