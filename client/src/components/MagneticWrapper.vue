<script setup lang="ts">
import { ref, onMounted, onUnmounted } from "vue";

interface Props {
  /** How far element moves toward the cursor (px) */
  strength?: number;
  /** How far the cursor can be from the element to start reacting (px) */
  range?: number;
  /** Optional class for the wrapper */
  className?: string;
}

const props = withDefaults(defineProps<Props>(), {
  strength: 30,
  range: 200,
  className: "",
});

const wrapper = ref<HTMLElement | null>(null);
const child = ref<HTMLElement | null>(null);

function handleMouseMove(e: MouseEvent) {
  if (!wrapper.value || !child.value) return;

  const rect = wrapper.value.getBoundingClientRect();
  const centerX = rect.left + rect.width / 2;
  const centerY = rect.top + rect.height / 2;

  const x = e.clientX - centerX;
  const y = e.clientY - centerY;
  const distance = Math.sqrt(x * x + y * y);

  if (distance < props.range) {
    // Normalize how close the cursor is (closer = stronger)
    const proximity = 1 - distance / props.range;
    const moveX = (x / rect.width) * props.strength * proximity;
    const moveY = (y / rect.height) * props.strength * proximity;

    child.value.style.transition = "transform 0.05s ease-out";
    child.value.style.transform = `translate(${moveX}px, ${moveY}px)`;
  } else {
    resetPosition();
  }
}

function resetPosition() {
  if (!child.value) return;
  child.value.style.transition = "transform 0.6s ease";
  child.value.style.transform = "translate(0, 0)";
}

onMounted(() => {
  window.addEventListener("mousemove", handleMouseMove);
  window.addEventListener("mouseleave", resetPosition);
});

onUnmounted(() => {
  window.removeEventListener("mousemove", handleMouseMove);
  window.removeEventListener("mouseleave", resetPosition);
});
</script>

<template>
  <div ref="wrapper" class="inline-block" :class="className">
    <div
      ref="child"
      class="transition-transform duration-300 ease-out will-change-transform"
    >
      <slot />
    </div>
  </div>
</template>
