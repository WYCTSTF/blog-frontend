<script setup>
</script>

<template>
  <header id="header">
    <div id="header-outer" class="outer">
      <div id="header-inner" class="inner">
        <nav id="main-nav">
          <a id="main-nav-toggle" class="nav-icon"></a>
          <router-link class="main-nav-link" to="/">Home</router-link>
          <router-link class="main-nav-link" to="/archives">Archives</router-link>
        </nav>
        <nav id="sub-nav">
          <a id="nav-search-btn" class="nav-icon" title="Search"></a>
        </nav>
        <div id="search-form-wrap">
          <!-- Search form placeholder -->
        </div>
      </div>
    </div>
    <div id="banner"></div>
    <div id="header-title" class="inner">
      <h1 id="logo-wrap">
        <a href="/" id="logo">My Blog</a>
      </h1>
      <h2 id="subtitle-wrap">
        <a href="/" id="subtitle">A Vue 3 Implementation of Hexo Landscape</a>
      </h2>
    </div>
  </header>
</template>

<style scoped>
#header {
  height: 300px;
  position: relative;
  border-bottom: 1px solid #ddd;
  background: #222;
  color: #fff;
}

#header-outer {
  height: 100%;
  position: relative;
}

#header-inner {
  position: relative;
  overflow: hidden;
}

#banner {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: url('https://via.placeholder.com/1920x300') center center;
  background-size: cover;
  z-index: -1;
  opacity: 0.4;
}

#header-title {
  text-align: center;
  height: 200px;
  position: absolute;
  top: 50%;
  left: 0;
  margin-top: -100px;
  width: 100%;
}

#logo {
  font-size: 40px;
  font-weight: bold;
  color: #fff;
  text-decoration: none;
}

#subtitle {
  font-size: 20px;
  color: #ddd;
  text-decoration: none;
}

#main-nav {
  float: left;
  margin-left: -20px;
}

.main-nav-link {
  color: #fff;
  text-decoration: none;
  padding: 20px;
  display: inline-block;
}

.main-nav-link:hover {
  background: rgba(255, 255, 255, 0.1);
}
</style>
