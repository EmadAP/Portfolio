<script setup lang="ts">
import Mouse from "./components/Mouse.vue";
import ScrollToTopBtn from "./components/ScrollToTopBtn.vue";
import Navbar from "./template/Navbar.vue";
</script>

<template>
  <div>
    <Navbar />

    <router-view />
    <Mouse />
    <ScrollToTopBtn />
  </div>
</template>
