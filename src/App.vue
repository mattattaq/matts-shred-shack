<script setup>
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
import Content from './components/Content.vue'
</script>

<template>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link
    href="https://fonts.googleapis.com/css2?family=Crimson+Pro:ital,wght@0,200..900;1,200..900&family=Metal+Mania&display=swap"
    rel="stylesheet">
  <Header />
  <Content />
  <Footer />
</template>

<style scoped>
body {
  width: 100%;
  height: auto;
  min-height: 500px;
}
</style>
