<script setup lang="ts">
import { IonChevronLeft, IonChevronRight } from "@twistify/vue3-icons/ion";

// No script logic needed; purely visual
</script>

<template>
  <div class="overflow-hidden whitespace-nowrap w-full h-full">
    <div
      class="inline-block animate-marquee text-[400px] leading-40 font-extrabold font-title text-stone-700 font-stretch-ultra-expanded"
    >
     
      <span
        v-for="n in 1"
        :key="n"
        class="mr-16 flex flex-row gap-8 w-full h-full items-center"
        ><IonChevronLeft :size="80" /> Frontend
        <IonChevronRight :size="80" /><IonChevronLeft :size="80" /> React
        <IonChevronRight :size="80" /><IonChevronLeft :size="80" />Next
        <IonChevronRight :size="80" /><IonChevronLeft :size="80" />Tailwind
        <IonChevronRight :size="80" /><IonChevronLeft :size="80" />Typescript
        <IonChevronRight :size="80" /><IonChevronLeft :size="80" />Javascript
        <IonChevronRight :size="80" /><IonChevronLeft :size="80" />Express
        <IonChevronRight :size="80" /><IonChevronLeft :size="80" />Vue
        <IonChevronRight :size="80" /><IonChevronLeft :size="80" />Mongodb
        <IonChevronRight :size="80" /><IonChevronLeft :size="80" />Css
        <IonChevronRight :size="80" /><IonChevronLeft :size="80" />Html
        <IonChevronLeft :size="80" />
      </span>
    </div>
  </div>
</template>

<style scoped>
@keyframes marquee {
  0% {
    transform: translateX(100%);
  }
  100% {
    transform: translateX(-100%);
  }
}

.animate-marquee {
  animation: marquee 70s linear infinite;
}
</style>
