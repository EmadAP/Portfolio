<script setup lang="ts">
import { ref, onMounted, onUnmounted } from "vue";
import { BiArrowUp } from "@twistify/vue3-icons/bi";

const isVisible = ref(false);

const handleScroll = () => {
  const scrollTop = window.scrollY || document.documentElement.scrollTop;
  isVisible.value = scrollTop > 200;
};

const scrollToTop = () => {
  window.scrollTo({ top: 0, behavior: "smooth" });
};

onMounted(() => {
  window.addEventListener("scroll", handleScroll);
});

onUnmounted(() => {
  window.removeEventListener("scroll", handleScroll);
});
</script>

<template>
  <transition name="fade">
    <button
      v-if="isVisible"
      @click="scrollToTop"
      class="fixed md:bottom-10 md:right-10 bottom-4 right-4 z-50 group w-36 h-36 rounded-full grid place-items-center cursor-pointer transition-transform duration-500 ease-in-out hover:-translate-y-3"
    >
      <div
        class="gradient element-to-rotate shadow-2xl from-sky-500 to-rose-500 via-violet-500 group-hover:duration-200 absolute transition-all duration-700 rounded-full -inset-px bg-gradient-to-r blur-lg opacity-80 group-hover:opacity-100 group-hover:-inset-1 animate-pulse"
      ></div>

      <BiArrowUp class="absolute text-5xl text-stone-900" />

      <svg class="w-36 h-36 text-circle rotate-[-90deg]" viewBox="0 0 100 100">
        <defs>
          <path
            id="circlePath"
            d="M 50, 50
               m -35, 0
               a 35,35 0 1,1 70,0
               a 35,35 0 1,1 -70,0"
          />
        </defs>
        <text fill="#000e17" font-size="7" font-weight="800" letter-spacing="2">
          <textPath href="#circlePath" startOffset="0%">
            SCROLL TO TOP •• SCROLL TO TOP ••
          </textPath>
        </text>
      </svg>
    </button>
  </transition>
</template>

<style scoped>
.text-circle {
  animation: spinText 20s linear infinite;
  transform-origin: center;
}

@keyframes spinText {
  to {
    transform: rotate(360deg);
  }
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s ease;
}
.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
</style>
