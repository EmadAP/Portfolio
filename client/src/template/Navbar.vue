<script lang="ts" setup>
import { ref, onMounted, onUnmounted } from "vue";
import { AiCloseOutlined, AiMenuOutlined } from "@twistify/vue3-icons/ai";
import { RaSlash } from "@twistify/vue3-icons/ra";
import { IonChevronLeft, IonChevronRight } from "@twistify/vue3-icons/ion";

const isScrolled = ref(false);
const isMenuOpen = ref(false);

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
  isMenuOpen.value = false;
}
</script>

<template>
  <div class="fixed w-full font-btn z-20">
    <div
      class="px-4 h-20 bg-stone-800 transition-all duration-700"
      :class="
        isScrolled
          ? 'mx-auto lg:mx-20 sm:mx-2 sm:rounded-xl  mt-6 bg-stone-800/90 backdrop-blur-lg'
          : 'mx-0'
      "
    >
      <div
        class="flex flex-row justify-between text-white items-center h-full transition-all duration-700"
      >
        <button class="cursor-pointer" @click="scrollToSection('home')">
          <div class="flex flex-row items-center relative">
            <IonChevronLeft :size="20" />
            <p class="text-3xl font-base">Emad Amoupour</p>
            <RaSlash :size="30" class="absolute -right-9" />

            <IonChevronRight :size="20" class="absolute -right-11" />
          </div>
        </button>

        <div class="lg:flex hidden flex-row items-center justify-center gap-6">
          <button class="Nav-Btn" @click="scrollToSection('home')">Home</button>
          <button class="Nav-Btn" @click="scrollToSection('projects')">
            Projects
          </button>
          <button class="Nav-Btn" @click="scrollToSection('about')">
            About
          </button>
          <button class="Nav-Btn" @click="scrollToSection('skills')">
            Skills
          </button>
          <button class="Nav-Btn" @click="scrollToSection('contact')">
            Contact
          </button>
        </div>

        <div class="lg:hidden flex">
          <AiMenuOutlined
            v-if="!isMenuOpen"
            :size="50"
            class="cursor-pointer p-3 hover:bg-stone-700 rounded-full"
            @click="isMenuOpen = true"
          />
          <AiCloseOutlined
            v-else
            :size="50"
            class="cursor-pointer p-3 hover:bg-stone-700 rounded-full"
            @click="isMenuOpen = false"
          />
        </div>
      </div>
      <transition name="fade">
        <div
          v-if="isMenuOpen"
          class="lg:hidden flex flex-col bg-stone-800 text-white mt-2 rounded-xl shadow-md p-4 space-y-3"
          :class="
            isScrolled ? 'mx-auto bg-stone-800/95 backdrop-blur-lg' : 'mx-0'
          "
        >
          <button
            class="Nav-Btn w-full text-left"
            @click="scrollToSection('home')"
          >
            Home
          </button>
          <button
            class="Nav-Btn w-full text-left"
            @click="scrollToSection('projects')"
          >
            Projects
          </button>
          <button
            class="Nav-Btn w-full text-left"
            @click="scrollToSection('about')"
          >
            About
          </button>
          <button
            class="Nav-Btn w-full text-left"
            @click="scrollToSection('skills')"
          >
            Skills
          </button>
          <button
            class="Nav-Btn w-full text-left"
            @click="scrollToSection('contact')"
          >
            Contact
          </button>
        </div>
      </transition>
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
  background: transparent;
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
  background-color: #57534d;
  border-radius: inherit;
  z-index: -1;
  transition: transform 0.4s ease-in-out;
  transform-origin: center;
}

.Nav-Btn:hover::before {
  transform: translate(-50%, -50%) scale(1);
}
</style>
