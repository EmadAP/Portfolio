<script setup lang="ts">
import { ref, onMounted } from "vue";
import ScrollToTopBtn from "./components/ScrollToTopBtn.vue";
import Navbar from "./template/Navbar.vue";
import Mouse from "./components/Mouse.vue";

const isDesktop = ref(false);

onMounted(() => {
  isDesktop.value = window.matchMedia("(pointer: fine)").matches;
});
</script>

<template>
  <div>
    <Navbar />
    <router-view />

    <Mouse v-if="isDesktop" />

    <ScrollToTopBtn />
  </div>
</template>
