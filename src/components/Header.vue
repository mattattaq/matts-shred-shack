<script setup>
import { ref } from 'vue'

defineProps({
  msg: String,
})

const count = ref(0)
</script>

<template>
  <header>
    <div class="container">
      <h1>Matt's Shred Shack!</h1>
      <ul>
        <li><a href="#about">About</a></li>
        <li><a href="#testimonials">Testimonials</a></li>
        <li><a href="#schedule">Schedule Your Lesson</a></li>
      </ul>
    </div>
  </header>
</template>

<style scoped>
header {
  height: 75px;
  background-color: black;
  width: 100%;
  min-width: 320px;
  position: fixed;
  scroll-behavior: smooth;
  top: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex: auto;
  z-index: 1;
}

header h1 {
  color: red;
  margin: 0;
  float: left;
  line-height: 75px;
  margin-right: 2%;
  transform: rotate(-5deg);
  font-family: "Metal Mania", serif;
  font-weight: 400;
  font-style: normal;
}

header ul {
  list-style: none;
  display: flex;
  gap: 20px;
  padding: 0;
  margin: 0;
  line-height: 75px;
}

header ul li {
  display: flex;
}

header ul li a {
  color: white;
  text-decoration: none;
}

header ul li a:hover {
  color: var(--yellow);
}

/* media queries */
@media screen and (max-width: 1024px) {
  header {
    min-height: 100px;
    height: auto;
  }

  h1 {
    font-size: 3em;
    display: block;
    width: 100%;
  }

  header ul {
    display: inline-flex;
  }

  header ul li {
    margin-left: 16px;
  }

}
</style>
