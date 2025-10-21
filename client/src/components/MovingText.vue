<script lang="ts" setup>
import { ref, onMounted, onBeforeUnmount } from "vue";
import { IonChevronLeft, IonChevronRight } from "@twistify/vue3-icons/ion";

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

const doubledSkills = [...skills, ...skills];

const marqueeRef = ref<HTMLElement | null>(null);
const duration = ref(14);

let lastScroll = window.scrollY;

const onScroll = () => {
  const currentScroll = window.scrollY;
  const delta = Math.abs(currentScroll - lastScroll);

  const newDuration = Math.max(2, 10 - delta / 20);
  duration.value = newDuration;

  lastScroll = currentScroll;
};

onMounted(() => {
  window.addEventListener("scroll", onScroll);
});

onBeforeUnmount(() => {
  window.removeEventListener("scroll", onScroll);
});
</script>

<template>
  <div
    class="pointer-events-none overflow-y-visible overflow-x-hidden w-full bg-stone-200 py-10 flex flex-row items-center"
  >
    <div
      ref="marqueeRef"
      class="pointer-events-none flex gap-4 whitespace-nowrap animate-marquee"
      :style="{ '--marquee-duration': duration + 's' }"
    >
      <div
        v-for="(skill, index) in doubledSkills"
        :key="index"
        class="pointer-events-none flex items-center gap-4 shrink-0"
      >
        <IonChevronLeft :size="40" />
        <span
          class="pointer-events-none text-[100px] font-extrabold font-btn text-stone-700 leading-none"
        >
          {{ skill }}
        </span>
        <IonChevronRight :size="40" />
      </div>
    </div>

    <div
      ref="marqueeRef"
      class="pointer-events-none flex gap-4 whitespace-nowrap animate-marquee"
      :style="{ '--marquee-duration': duration + 's' }"
    >
      <div
        v-for="(skill, index) in doubledSkills"
        :key="index"
        class="flex items-center gap-4 shrink-0"
      >
        <IonChevronLeft :size="40" />
        <span
          class="pointer-events-none text-[100px] font-extrabold font-btn text-stone-700 leading-none"
        >
          {{ skill }}
        </span>
        <IonChevronRight :size="40" />
      </div>
    </div>
  </div>
</template>

<style scoped>
@keyframes marquee {
  0% {
    transform: translateX(0%);
  }
  100% {
    transform: translateX(-50%);
  }
}

.animate-marquee {
  display: flex;
  animation: marquee linear infinite;
  animation-duration: var(--marquee-duration);
}
</style>
