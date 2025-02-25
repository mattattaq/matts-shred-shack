<script setup>

</script>

<template>
  <footer>
    <section id="footer">
      <div class="container">
        <ul>
          <li>LinkedIN</li>
          <li>GitHub</li>
          <li></li>
        </ul>
      </div>
    </section>
  </footer>
</template>

<style scoped>
footer {
  background-color: white;
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
  background-image: url("../assets/notes.jpg");
  min-height: 300px;
  width: 100%;
  position: relative;
}
</style>
