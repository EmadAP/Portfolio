<script setup lang="ts">
import { IonChevronLeft, IonChevronRight } from "@twistify/vue3-icons/ion";

import { ref, onMounted, onUnmounted, watch } from "vue";

const skills = [
  "Frontend",
  "React",
  "Next",
  "Tailwind",
  "Typescript",
  "Javascript",
  "Express",
  "Vue",
  "Mongodb",
  "Css",
  "Html",
];

const speed = ref(70);
let lastScrollY = 0;
let ticking = false;

// Scroll handler to adjust speed
function handleScroll() {
  const currentScrollY = window.scrollY;
  const delta = Math.abs(currentScrollY - lastScrollY);

  // Map delta to new speed: faster scroll → shorter duration → faster animation
  speed.value = Math.max(20, 70 - delta * 0.5);

  lastScrollY = currentScrollY;

  if (!ticking) {
    window.requestAnimationFrame(() => {
      ticking = false;
    });
    ticking = true;
  }
}

onMounted(() => {
  window.addEventListener("scroll", handleScroll);
});

onUnmounted(() => {
  window.removeEventListener("scroll", handleScroll);
});
</script>

<template>
  <div
    class="relative w-screen h-[200px] overflow-hidden bg-stone-200 flex items-center"
  >
    <!-- Fade mask on left/right -->
    <div
      class="absolute inset-0 pointer-events-none [mask-image:linear-gradient(to_right,transparent,black 20%,black 80%,transparent)] z-10"
    ></div>

    <!-- Moving container -->
    <div class="flex will-change-transform whitespace-nowrap animate-marquee">
      <!-- Repeat content twice for seamless loop -->
      <div
        v-for="repeat in 200"
        :key="repeat"
        class="flex flex-row items-center gap-16"
      >
        <template v-for="(skill, index) in skills" :key="index">
          <IonChevronLeft :size="60" />
          <span
            class="text-[150px] font-extrabold font-title text-stone-700 leading-none"
          >
            {{ skill }}
          </span>
          <IonChevronRight :size="60" />
        </template>
      </div>
    </div>
  </div>
</template>


<style scoped>
@keyframes marquee {
  from {
    transform: translateX(0);
  }
  to {
    transform: translateX(-50%);
  }
}

/* Infinite scrolling */
.animate-marquee {
  animation: marquee 70s linear infinite;
}
</style>
