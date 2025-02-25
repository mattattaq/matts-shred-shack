<script setup>
import notes from '@/assets/notes.jpg';

const notesUrl = notes;

</script>

<template>
  <footer>
    <!-- background-image: url("../assets/notes.jpg"); -->
    <section id="footer" :style="{ backgroundImage: `url(${notesUrl})` }">
      <div class="container">
        <ul>
          <li><a href="#about">About</a></li>
          <!-- <li><a href="#testimonials">Testimonials</a></li> -->
          <li><a href="#lesson">Book a Lesson</a></li>
          <li><a href="https://www.linkedin.com/in/matthew-allbright-b4896749/" target="_blank">LinkedIN</a></li>
        </ul>
        <blockquote>"Shred Hard, Play Loud, Stay Metal!"</blockquote>
        <p>© 2025 Matt's Shred Shack. All Rights Reserved.</p>
      </div>
    </section>
  </footer>
</template>

<style scoped>
footer {
  background-color: white;
}

blockquote {
  font-family: "Metal Mania", serif;
  font-weight: 400;
  font-style: normal;
}

#footer::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(255, 255, 255, 0.6);
}

#footer {
  background-position: center;
  background-size: cover;
  min-height: 200px;
  padding-top: 8px;
  width: 100%;
  position: relative;
}

footer ul {
  list-style: none;
}

footer ul li a {
  font-size: bold;
  text-decoration: none;
  color: black;
}

footer ul li a:hover {
  color: var(--yellow);
}

footer p {
  font-size: 1em;
}
</style>
