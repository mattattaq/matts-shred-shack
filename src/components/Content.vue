<script setup>
import { onMounted } from 'vue';

const splashUrl = '../splash.jpg';
const teacherUrl = '../meet-your-teacher.jpg';
const winterUrl = '../sg-winter.jpg';
const fenderSplashUrl = '../fender-splash.jpg';

onMounted(() => {
  const elements = document.querySelectorAll('.fade-in');

  const observer = new IntersectionObserver(
    (entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          entry.target.classList.add('visible');
        }
      });
    },
    { threshold: 0.3 } // Element becomes visible when 30% of it is in view
  );

  elements.forEach((el) => observer.observe(el));
});
</script>

<template>
  <section id="top" :style="{ backgroundImage: `url(${splashUrl})` }">
    <div class="container">
      <h2>Your Shred Journey Starts Here!</h2>
      <p class="bottom fade-in">
        Want to master face-melting solos, crushing riffs, and precision techniques? Book a <a
          href="https://calendly.com/mattatttaq/30-minute-lesson" target="_blank">lesson now</a>
        and let’s make
        some noise!
      </p>
    </div>
  </section>
  <section id="about">
    <div class="container">
      <div class="half">
        <h3>Meet your teacher:</h3>
        <p class="fade-in">Hey, I’m Matt, a guitarist based in Indianapolis, and I’ve been shredding since 2015. I
          specialize in rock
          and metal, dialing in everything from crushing riffs to lightning-fast solos. Whether it's tight rhythm
          playing or expressive lead work, I love pushing the boundaries of what the guitar can do.
          <br>
          When I’m not teaching, you’ll find me on stage with my band, <i>Curls Just Wanna Have Fun</i>, bringing
          high-energy
          performances to local venues. Playing live has given me a deep understanding of tone, technique, and stage
          presence—skills I love sharing with my students. Whether you're picking up the guitar for the first time or
          refining your chops, I’m here to help you unlock your full potential. Let’s make some noise!
        </p>
      </div>
      <div class="half">
        <img :src="teacherUrl" alt="It's me, Matthew Allbright">
      </div>
    </div>
  </section>
  <section id="middle" :style="{ backgroundImage: `url(${fenderSplashUrl})` }">
    <div class="container">
      <p class="bottom fade-in">
        What you'll learn.
      </p>
      <ul>
        <li class="bottom fade-in"> Essential Guitar Techniques – Master picking, fretting, and finger strength to build
          a solid foundation.</li>
        <li class="bottom fade-in">Rock & Metal Techniques – Master palm muting, alternate picking, downpicking, and
          high-speed shredding.</li>
        <li class="bottom fade-in">Rock & Metal Riffs – Learn iconic riffs and create crushing rhythms with tight,
          aggressive playing.</li>
        <li class="bottom fade-in">Shredding & Speed Building – Develop blazing-fast alternate picking, sweep picking,
          and legato techniques.</li>
        <li class="bottom fade-in">Soloing & Improvisation – Craft expressive solos with scales, phrasing, and
          emotional dynamics.</li>
        <li class="bottom fade-in">Tone & Gear Advice – Get insights on amps, pedals, and effects to shape your
          signature tone.</li>
        <li class="bottom fade-in">Live Performance Skills – Gain confidence playing in a band, on stage, or in front of
          an audience.
        </li>
      </ul>
    </div>
  </section>
  <!-- <section id="testimonials">
    <div class="container"></div>
  </section> -->
  <section id="lesson">
    <div class="container">
      <div class="half hide-on-mobile">
        <img :src="winterUrl" alt="It's me, Matthew Allbright">
      </div>
      <div class="half">
        <h3>Lessons & Pricing</h3>
        <p>My lessons are held over Zoom, making it easy for you to learn from anywhere. Whether you're just starting or
          looking to refine your skills, I offer flexible lesson options:</p>
        <p>🎸 30-Minute Lesson – $30 (Perfect for quick progress and focused learning)</p>
        <p>🔥 1-Hour Lesson – $55 (More in-depth instruction and hands-on practice)</p>
        <h3>How it works</h3>
        <ol>
          <li><b>Pick Your Lesson Length</b> – Choose between a 30-minute or 1-hour session.</li>
          <li><b>Schedule Your Lesson</b> – Book your time slot using the link below.</li>
          <li><b>Join the Zoom Call</b> – I'll send you a link before the lesson, and we’ll dive into your guitar goals!
          </li>
          <a class="button" href="https://calendly.com/mattatttaq" target="_blank">Schedule Now!</a>
        </ol>
      </div>
    </div>
  </section>
</template>

<style scoped>
section {
  min-height: 300px;
  height: auto;
}

.read-the-docs {
  color: #888;
}

.fade-in {
  opacity: 0;
  transform: translateY(20px);
  transition: opacity 0.8s ease-out, transform 0.8s ease-out;
}

@keyframes pulse {
  0% {
    transform: scale(1);
    box-shadow: 0 0 5px var(--yellow);
  }

  50% {
    transform: scale(1.05);
    box-shadow: 0 0 15px var(--yellow);
  }

  100% {
    transform: scale(1);
    box-shadow: 0 0 5px var(--yellow);
  }
}

.button {
  background-color: var(--yellow);
  padding: 8px 8px;
  margin-top: 8px;
  display: block;
  width: 200px;
  text-align: center;
  border-radius: 8px;
  font-size: 1em;
  font-weight: bold;
  text-decoration: none;
  color: black;
  transition: transform 0.2s ease-in-out;
  animation: pulse 1.5s infinite ease-in-out;
}

.fade-in.visible {
  opacity: 1;
  transform: translateY(0);
}

.bottom {
  align-self: flex-end;
  margin-top: auto;
}

.half {
  flex: 1;
  max-width: 50%;
  box-sizing: border-box;
  float: left;
}

.half img {
  width: calc(100% - 16px);
  margin: 8px 8px;
}

/* top section */
#top {
  background-size: cover;
  height: 100%;
  min-height: 600px;
  margin-top: 75px;
}

/* middle section */

#middle {
  background-size: cover;
  height: 100%;
  min-height: 600px;
}

#middle ul {
  list-style: none;
}

#middle li {
  margin-top: 16px;
}

#middle p {
  margin-top: 50px;
}

/* top section */
#top h2 {
  margin-top: 25px;
}

#top h2,
.bottom {
  background-color: black;
  width: 50%;
  padding-left: 2%;
  color: white;
}

#top .container {
  min-height: 600px !important;
  display: flex;
  flex-direction: column;
}

#top a {
  color: var(--yellow);
}

/* about section */
#about .container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
}

/* lesson section */
#lesson {
  height: 100%;
  display: flex;
}

/* media queries */
@media screen and (max-width: 1024px) {
  .half {
    max-width: 100%;
    width: 100%;
    clear: both;
    padding: 8px;
    flex: none;
  }

  .hide-on-mobile {
    display: none;
  }

  .button {
    width: 80%;
  }
}
</style>
