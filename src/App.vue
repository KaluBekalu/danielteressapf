<script setup>
import Header from "./views/Header.vue";
import About from "./views/About.vue";
import Contact from "./views/Contact.vue";
import Education from "./views/Education.vue";
import Experiences from "./views/Experiences.vue";
import Certifications from "./views/Certifications.vue";
import Footer from "./views/Footer.vue";
import cv from "../cv";
</script>

<template>
  <div class="box">
    <Header />
    <About :personalInfo="cv.personalInfo" />
    <Experiences :experiences="cv.experiences" />
    <Education :educations="cv.educations" />
    <Certifications :certifications="cv.certifications" />
    <Contact :personalInfo="cv.personalInfo" />
    <Footer />
  </div>
</template>

<style>
html {
  font-family: "Blinker", sans-serif;
  scroll-behavior: smooth;
}

*,
#app {
  margin: 0;
  padding: 0;
}

.box {
  display: flex;
  flex-direction: column;
  gap: 5rem;
}
/*
:target::before {
  display: block;
  content: "";
  margin: 5rem;
}
*/


#experiences::before,
#education::before,
#certifications::before,
#contact::before {
  display: block;
  content: "";
  height: 5rem;
}

.container {
  width: 90%;
  margin-inline: auto;
  box-sizing: border-box;
}

@media (min-width: 1400px) {
  #app {
    max-width: 1400px;
    margin: auto;
  }
}
@media (max-width: 950px) {
  .container {
    width: 100%;
    margin-inline: auto;
    box-sizing: border-box;
  }
}
</style>
