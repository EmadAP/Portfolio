<script lang="ts" setup>
import AboutPage from "./AboutPage.vue";
import ContactPage from "./ContactPage.vue";
import HomePage from "./HomePage.vue";
import ProjectsPage from "./ProjectsPage.vue";
import SkillsPage from "./SkillsPage.vue";
</script>
<template>
  <div id="home">
    <HomePage />
  </div>
  <div class="h-2 bg-stone-900"></div>

  <div id="projects">
    <ProjectsPage />
  </div>
  <div class="h-2 bg-stone-900"></div>

  <div id="about">
    <AboutPage />
  </div>
  <div class="h-2 bg-stone-900"></div>

  <div id="skills">
    <SkillsPage />
  </div>
  <div class="h-2 bg-stone-900"></div>

  <div id="contact">
    <ContactPage />
  </div>
</template>
