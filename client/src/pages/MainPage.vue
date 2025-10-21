<script lang="ts" setup>
import AboutPage from "./AboutPage.vue";
import ContactPage from "./ContactPage.vue";
import HomePage from "./HomePage.vue";
import ProjectsPage from "./ProjectsPage.vue";
import ResumePage from "./ResumePage.vue";
import SkillsPage from "./SkillsPage.vue";
</script>
<template>
    <HomePage id="home" />

  <div class="h-2 bg-stone-900"></div>

  <ProjectsPage id="projects" />

  <div class="h-2 bg-stone-900"></div>

  <AboutPage id="about" />

  <div class="h-2 bg-stone-900"></div>

  <SkillsPage id="skills" />

  <div class="h-2 bg-stone-900"></div>

  <ResumePage id="resumeNav" />

  <div class="h-2 bg-stone-900"></div>

  <ContactPage id="contact" />

  <div class="h-2 bg-stone-900"></div>
</template>
