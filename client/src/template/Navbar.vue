<script lang="ts" setup>
import { ref, onMounted, onUnmounted } from "vue";
import { ChevronLeft, ChevronRight, Menu, Slash } from "lucide-vue-next";

const isScrolled = ref(false);

function handleScroll() {
  isScrolled.value = window.scrollY > 0;
}

onMounted(() => {
  window.addEventListener("scroll", handleScroll);
});

onUnmounted(() => {
  window.removeEventListener("scroll", handleScroll);
});

function scrollToSection(id: string) {
  const el = document.getElementById(id);
  if (el) {
    el.scrollIntoView({ behavior: "smooth" });
  }
}
</script>

<template>
  <div
    class="font-btn sticky z-20 inset-x-0 top-0 px-4 h-20 bg-stone-800 transition-all duration-700"
    :class="
      isScrolled ? 'mx-auto sm:mx-5 lg:mx-20 sm:rounded-xl top-9   bg-stone-800/85 backdrop-blur-lg' : 'mx-0'
    "
  >
    <div
      class="flex flex-row justify-between text-white items-center h-full transition-all duration-700"
    >
      <button class="cursor-pointer" @click="scrollToSection('home')">
        <div class="flex flex-row items-center">
          <ChevronLeft />
          <p class="text-3xl font-base">Emad Amoupour</p>
          <Slash class="-rotate-[20deg]" />
          <ChevronRight />
        </div>
      </button>

      <div class="lg:flex hidden flex-row items-center justify-center gap-6">
        <button class="Nav-Btn" @click="scrollToSection('home')">Home</button>
        <button class="Nav-Btn" @click="scrollToSection('projects')">
          Projects
        </button>
        <button class="Nav-Btn" @click="scrollToSection('about')">About</button>
        <button class="Nav-Btn" @click="scrollToSection('skills')">
          Skills
        </button>
        <button class="Nav-Btn" @click="scrollToSection('contact')">
          Contact
        </button>
      </div>

      <div class="lg:hidden flex">
        <Menu />
      </div>
    </div>
  </div>
</template>

<style>
.Nav-Btn {
  position: relative;
  padding: 6px 12px;
  font-size: 20px;
  font-weight: 550;
  cursor: pointer;
  border-radius: 8px;
  border: none;
  background: #292524;
  overflow: hidden;
  z-index: 1;
}

.Nav-Btn::before {
  content: "";
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%) scale(0);
  width: 100%;
  height: 100%;
  background-color: #44403b;
  border-radius: inherit;
  z-index: -1;
  transition: transform 0.4s ease-in-out;
  transform-origin: center;
}

.Nav-Btn:hover::before {
  transform: translate(-50%, -50%) scale(1);
}
</style>
