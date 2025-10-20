<script lang="ts" setup>
import AboutPage from "./AboutPage.vue";
import ContactPage from "./ContactPage.vue";
import HomePage from "./HomePage.vue";
import ProjectsPage from "./ProjectsPage.vue";
import SkillsPage from "./SkillsPage.vue";
</script>
<template>
  <HomePage id="home" />

  <div class="h-2 bg-stone-900"></div>

  <ProjectsPage id="projects" />

  <div class="h-2 bg-stone-900"></div>

  <AboutPage id="about" />

  <div class="h-2 bg-stone-900"></div>
  <!-- we have scroll width problem here  -->
  <SkillsPage id="skills" />

  <div class="h-2 bg-stone-900"></div>

  <ContactPage id="contact" />
</template>
