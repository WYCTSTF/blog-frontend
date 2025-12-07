<script setup>
defineProps({
  post: {
    type: Object,
    required: true
  },
  isDetail: {
    type: Boolean,
    default: false
  }
})
</script>

<template>
  <article class="article">
    <div class="article-meta">
      <a href="#" class="article-date">
        <time :datetime="post.date">{{ post.date }}</time>
      </a>
      <div class="article-category" v-if="post.category">
        <a class="article-category-link" href="#">{{ post.category }}</a>
      </div>
    </div>
    <div class="article-inner">
      <header class="article-header">
        <h1 v-if="isDetail" class="article-title">{{ post.title }}</h1>
        <h1 v-else class="article-title">
          <router-link :to="'/post/' + post.id">{{ post.title }}</router-link>
        </h1>
      </header>
      <div class="article-entry">
        <p v-if="!isDetail">{{ post.excerpt }}</p>
        <div v-else v-html="post.content"></div>
        
        <p v-if="!isDetail" class="article-more-link">
          <router-link :to="'/post/' + post.id">Read More</router-link>
        </p>
      </div>
      <footer class="article-footer">
        <a href="#" class="article-share-link">Share</a>
        <a href="#" class="article-comment-link">Comments</a>
        <ul class="article-tag-list" v-if="post.tags">
          <li class="article-tag-list-item" v-for="tag in post.tags" :key="tag">
            <a class="article-tag-list-link" href="#">{{ tag }}</a>
          </li>
        </ul>
      </footer>
    </div>
  </article>
</template>

<style scoped>
.article {
  margin: 40px 0;
  background: #fff;
  box-shadow: 0 1px 2px rgba(0,0,0,0.05);
  border-radius: 3px;
}

.article-inner {
  padding: 20px;
  overflow: hidden;
}

.article-meta {
  float: left;
  margin-right: 20px;
  width: 15%;
  text-align: right;
  display: none; /* Hidden on mobile usually, but let's keep simple */
}

@media (min-width: 768px) {
  .article-meta {
    display: block;
  }
}

.article-date {
  color: #999;
  text-decoration: none;
  display: block;
  margin-bottom: 0.5em;
}

.article-category-link {
  color: #999;
  text-decoration: none;
  text-transform: uppercase;
}

.article-header {
  margin-bottom: 20px;
}

.article-title {
  font-size: 2em;
  font-weight: bold;
  line-height: 1.1em;
  margin: 0;
}

.article-title a {
  color: #333;
  text-decoration: none;
}

.article-title a:hover {
  color: #258fb8;
}

.article-entry {
  color: #555;
  line-height: 1.8;
  margin-bottom: 20px;
}

.article-more-link a {
  color: #258fb8;
  text-decoration: none;
  border-bottom: 1px solid #258fb8;
}

.article-footer {
  font-size: 0.85em;
  line-height: 1.6em;
  border-top: 1px solid #ddd;
  padding-top: 1.6em;
  margin: 0;
}

.article-tag-list {
  list-style: none;
  padding: 0;
  display: inline-block;
  margin: 0;
}

.article-tag-list-item {
  display: inline-block;
  margin-right: 10px;
}

.article-tag-list-link {
  color: #999;
  text-decoration: none;
}
</style>
