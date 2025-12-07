<script setup>
import PostArticle from '../components/PostArticle.vue'
import { ref } from 'vue'

// Mock data
const posts = ref([
  {
    id: 1,
    title: 'Hello World',
    date: '2023-10-27',
    category: 'Tech',
    excerpt: 'Welcome to my new blog built with Vue 3. This is a sample post to demonstrate the layout.',
    tags: ['Vue', 'Hexo']
  },
  {
    id: 2,
    title: 'Another Post',
    date: '2023-10-28',
    category: 'Life',
    excerpt: 'This is another post. The layout is responsive and mimics the Hexo Landscape theme.',
    tags: ['Life', 'Thoughts']
  }
])
</script>

<template>
  <div class="home">
    <PostArticle v-for="post in posts" :key="post.id" :post="post" />
    
    <nav id="page-nav">
      <a class="extend prev" rel="prev" href="#">&laquo; Prev</a>
      <span class="page-number current">1</span>
      <a class="page-number" href="#">2</a>
      <a class="extend next" rel="next" href="#">Next &raquo;</a>
    </nav>
  </div>
</template>

<style scoped>
#page-nav {
  margin: 40px auto;
  background: #fff;
  box-shadow: 0 1px 2px rgba(0,0,0,0.05);
  border-radius: 3px;
  text-align: center;
  color: #555;
  overflow: hidden;
}

#page-nav a, #page-nav span {
  padding: 10px 20px;
  line-height: 1;
  height: 36px;
  display: inline-block;
  text-decoration: none;
  color: #555;
}

#page-nav a:hover, #page-nav span.current {
  background: #ddd;
  color: #333;
}
</style>
