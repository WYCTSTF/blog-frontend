<script setup>
import PostArticle from '../components/PostArticle.vue'
import { ref, onMounted } from 'vue'
import { useRoute } from 'vue-router'

const route = useRoute()
const post = ref(null)

onMounted(() => {
  // In a real app, fetch post by ID
  // For now, just mock it
  post.value = {
    id: route.params.id,
    title: 'Detailed Post Title',
    date: '2023-10-27',
    category: 'Tech',
    content: '<p>This is the full content of the post. It would typically be rendered from Markdown.</p><p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>',
    tags: ['Vue', 'Hexo']
  }
})
</script>

<template>
  <div class="post-view">
    <PostArticle v-if="post" :post="post" :isDetail="true" />
  </div>
</template>
