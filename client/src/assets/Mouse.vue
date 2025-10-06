<script setup lang="ts">
import { ref, onMounted, onUnmounted } from "vue";

const cursorX = ref(window.innerWidth / 2);
const cursorY = ref(window.innerHeight / 2);

const circleX = ref(cursorX.value);
const circleY = ref(cursorY.value);

const isHoveringText = ref(false); // <-- NEW state

let animationFrame: number;

// Lerp for smooth follow
function lerp(start: number, end: number, factor: number) {
  return start + (end - start) * factor;
}

function animate() {
  circleX.value = lerp(circleX.value, cursorX.value, 0.1);
  circleY.value = lerp(circleY.value, cursorY.value, 0.1);
  animationFrame = requestAnimationFrame(animate);
}

function handleMouseMove(e: MouseEvent) {
  cursorX.value = e.clientX;
  cursorY.value = e.clientY;
}

function handleMouseOver(e: MouseEvent) {
  const target = e.target as HTMLElement;
  if (target.matches("p, button, span, h1, h3")) {
    isHoveringText.value = true;
  }
}

function handleMouseOut(e: MouseEvent) {
  const target = e.target as HTMLElement;
  if (target.matches("p, button, span, h1, h3")) {
    isHoveringText.value = false;
  }
}

onMounted(() => {
  window.addEventListener("mousemove", handleMouseMove);
  window.addEventListener("mouseover", handleMouseOver);
  window.addEventListener("mouseout", handleMouseOut);
  animate();
});

onUnmounted(() => {
  cancelAnimationFrame(animationFrame);
  window.removeEventListener("mousemove", handleMouseMove);
  window.removeEventListener("mouseover", handleMouseOver);
  window.removeEventListener("mouseout", handleMouseOut);
});
</script>

<template>
  <!-- Circle Follower -->
  <div
    class="z-100 pointer-events-none fixed rounded-full bg-white mix-blend-difference transition-all duration-100 ease-in-out"
    :class="isHoveringText ? 'w-24 h-24 -top-4 -left-4' : 'w-10 h-10 top-3 left-3'"
    :style="{
      transform: `translate(${circleX - 32}px, ${circleY - 32}px)`,
    }"
  />
</template>
