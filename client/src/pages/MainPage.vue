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

  <div id="projects" class="h-2 bg-stone-900"></div>

  <ProjectsPage />

  <div id="about" class="h-2 bg-stone-900"></div>

  <AboutPage />

  <div id="skills" class="h-2 bg-stone-900"></div>

  <SkillsPage />

  <div id="contact" class="h-2 bg-stone-900"></div>

  <ContactPage />
</template>
