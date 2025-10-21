<script setup lang="ts">
import { defineProps } from "vue";

interface Props {
  label: string;
  icon: any;
  smallRadius?: number;
  bigRadius?: number;
}

const props = defineProps<Props>();

const smallRadius = props.smallRadius ?? 60;
const bigRadius = props.bigRadius ?? 75;

const smallIconsCount = 8;
const bigIconCount = 12;

const smallAngles = Array.from(
  { length: smallIconsCount },
  (_, i) => (360 / smallIconsCount) * i
);
const bigAngles = Array.from(
  { length: bigIconCount },
  (_, i) => (360 / bigIconCount) * i
);
</script>

<template>
  <div class="relative flex items-center justify-center group">
    <div
      class="absolute inset-0 flex items-center justify-center pointer-events-none opacity-0 group-hover:opacity-100 transition-opacity duration-300"
    >
      <div class="absolute w-0 h-0 spin-slow">
        <div
          v-for="(angle, i) in smallAngles"
          :key="'small-' + i"
          :style="{ transform: `rotate(${angle}deg)` }"
        >
          <component
            :is="props.icon"
            class="absolute w-6 h-6 text-stone-700"
            :style="{ transform: `translate(${smallRadius}px, 0)` }"
          />
        </div>
      </div>

      <div class="absolute w-0 h-0 spin-slower">
        <div
          v-for="(angle, i) in bigAngles"
          :key="'big-' + i"
          :style="{ transform: `rotate(${angle}deg)` }"
        >
          <component
            :is="props.icon"
            class="absolute w-10 h-10 text-stone-700"
            :style="{ transform: `translate(${bigRadius}px, 0)` }"
          />
        </div>
      </div>
    </div>

    <button
      class="cursor-pointer px-6 py-2 text-2xl text-stone-200 bg-stone-800 group-hover:bg-stone-700 rounded-xl shadow-2xl group-hover:scale-105 transition-transform duration-300"
    >
      {{ props.label }}
    </button>
  </div>
</template>

<style scoped>
@keyframes spin {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}

.absolute.spin-slow {
  animation: spin 15s linear infinite;
  transform-origin: center center;
}

.absolute.spin-slower {
  animation: spin 25s linear infinite;
  transform-origin: center center;
}
</style>
