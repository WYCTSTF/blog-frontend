<script setup>
import { RouterView } from 'vue-router'
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
import Sidebar from './components/Sidebar.vue'
</script>

<template>
  <div id="app-container">
    <Header />
    <div class="outer">
      <section id="main">
        <RouterView />
      </section>
      <Sidebar />
    </div>
    <Footer />
  </div>
</template>

<style>
/* Global layout styles */
.outer {
  max-width: 960px;
  margin: 0 auto;
  padding: 0 20px;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}

#main {
  flex: 1;
  min-width: 0; /* Fix flex item overflow */
  margin-right: 20px;
}

@media (max-width: 768px) {
  .outer {
    flex-direction: column;
  }
  #main {
    margin-right: 0;
  }
}
</style>
