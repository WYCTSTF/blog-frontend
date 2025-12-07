<script setup>
</script>

<template>
  <footer id="footer">
    <div class="outer">
      <div id="footer-info" class="inner">
        &copy; {{ new Date().getFullYear() }} My Blog<br>
        Powered by <a href="https://vuejs.org/" target="_blank">Vue 3</a>
      </div>
    </div>
  </footer>
</template>

<style scoped>
#footer {
  background: #262a30;
  padding: 50px 0;
  border-top: 1px solid #ddd;
  color: #999;
}
#footer a {
  color: #999;
  text-decoration: none;
}
#footer a:hover {
  text-decoration: underline;
}
#footer-info {
  line-height: 1.6;
  text-align: center;
}
</style>
