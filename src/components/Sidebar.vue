<script setup>
</script>

<template>
  <aside id="sidebar">
    <div class="widget-wrap">
      <h3 class="widget-title">Categories</h3>
      <div class="widget">
        <ul class="category-list">
          <li class="category-list-item"><a class="category-list-link" href="#">Tech</a></li>
          <li class="category-list-item"><a class="category-list-link" href="#">Life</a></li>
        </ul>
      </div>
    </div>

    <div class="widget-wrap">
      <h3 class="widget-title">Recent Posts</h3>
      <div class="widget">
        <ul>
          <li>
            <a href="#">Hello World</a>
          </li>
          <li>
            <a href="#">Vue 3 is Awesome</a>
          </li>
        </ul>
      </div>
    </div>
    
    <div class="widget-wrap">
      <h3 class="widget-title">Tags</h3>
      <div class="widget">
        <ul class="tag-list">
          <li class="tag-list-item"><a class="tag-list-link" href="#">Vue</a></li>
          <li class="tag-list-item"><a class="tag-list-link" href="#">JavaScript</a></li>
        </ul>
      </div>
    </div>
  </aside>
</template>

<style scoped>
#sidebar {
  width: 280px;
  line-height: 1.6em;
}

.widget-wrap {
  margin: 40px 0;
}

.widget-title {
  color: #ccc;
  text-transform: uppercase;
  letter-spacing: 2px;
  margin-bottom: 1em;
  line-height: 1em;
  font-weight: bold;
}

.widget {
  color: #777;
  background: #fff;
  box-shadow: 0 1px 2px rgba(0,0,0,0.05);
  padding: 15px;
  border-radius: 3px;
}

.widget ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

.widget ul li {
  margin: 5px 0;
}

.widget a {
  color: #777;
  text-decoration: none;
}

.widget a:hover {
  text-decoration: underline;
}
</style>
