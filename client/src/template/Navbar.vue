<script lang="ts" setup>
import { ref, onMounted, onUnmounted } from "vue";
import { AiCloseOutlined, AiMenuOutlined } from "@twistify/vue3-icons/ai";
import { RaSlash } from "@twistify/vue3-icons/ra";
import { IonChevronLeft, IonChevronRight } from "@twistify/vue3-icons/ion";
import HamburgerButton from "@/components/HamburgerButton.vue";

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
          ? 'mx-auto lg:mx-10 xl:mx-20 sm:mx-2 md:mx-10 sm:rounded-xl  mt-6 bg-stone-800/90 backdrop-blur-lg'
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

        <div class="lg:flex hidden flex-row items-center justify-center gap-8">
          <button
            class="px-2 py-2 text-xl font-semibold cursor-pointer border-b-4 bg-transparent border-b-transparent hover:border-b-stone-200 transform duration-300"
            @click="scrollToSection('home')"
          >
            Home
          </button>
          <button
            class="px-2 py-2 text-xl font-semibold cursor-pointer border-b-4 bg-transparent border-b-transparent hover:border-b-stone-200 transform duration-300"
            @click="scrollToSection('projects')"
          >
            Projects
          </button>
          <button
            class="px-2 py-2 text-xl font-semibold cursor-pointer border-b-4 bg-transparent border-b-transparent hover:border-b-stone-200 transform duration-300"
            @click="scrollToSection('about')"
          >
            About
          </button>
          <button
            class="px-2 py-2 text-xl font-semibold cursor-pointer border-b-4 bg-transparent border-b-transparent hover:border-b-stone-200 transform duration-300"
            @click="scrollToSection('skills')"
          >
            Skills
          </button>
          <button
            class="px-2 py-2 text-xl font-semibold cursor-pointer border-b-4 bg-transparent border-b-transparent hover:border-b-stone-200 transform duration-300"
            @click="scrollToSection('resumeNav')"
          >
            Resume
          </button>
          <button
            class="px-2 py-2 text-xl font-semibold cursor-pointer border-b-4 bg-transparent border-b-transparent hover:border-b-stone-200 transform duration-300"
            @click="scrollToSection('contact')"
          >
            Contact
          </button>
        </div>
<!-- 
        <button
          class="group lg:hidden flex h-20 w-20 cursor-pointer items-center justify-center bg-white p-3 hover:bg-stone-700 rounded-full"
        >
          <div class="space-y-2">
            <span
            v-if="!isMenuOpen"
              class="block h-1 w-10 origin-center rounded-full bg-sky-400 transition-transform ease-in-out group-hover:translate-y-1.5 group-hover:rotate-45"
              @click="isMenuOpen = true"
            ></span>
            <span
            v-else
              class="block h-1 w-8 origin-center rounded-full bg-rose-400 transition-transform ease-in-out group-hover:w-10 group-hover:-translate-y-1.5 group-hover:-rotate-45"
              @click="isMenuOpen = false"
            ></span>
          </div>
        </button> -->
        <div class="lg:hidden flex"><AiMenuOutlined
            v-if="!isMenuOpen"
            :size="50"
            class="cursor-pointer p-3 hover:bg-stone-700 rounded-full transition-all duration-400"
            @click="isMenuOpen = true"
          />
          <AiCloseOutlined
            v-else
            :size="50"
            class="cursor-pointer p-3 hover:bg-stone-700 rounded-full transition-all duration-400"
            @click="isMenuOpen = false"
          /></div>
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
            class="px-2 py-2 text-xl font-semibold cursor-pointer border-b-4 bg-transparent border-b-transparent hover:border-b-stone-200 transform duration-300 w-full text-center"
            @click="scrollToSection('home')"
          >
            Home
          </button>
          <button
            class="px-2 py-2 text-xl font-semibold cursor-pointer border-b-4 bg-transparent border-b-transparent hover:border-b-stone-200 transform duration-300 w-full text-center"
            @click="scrollToSection('projects')"
          >
            Projects
          </button>
          <button
            class="px-2 py-2 text-xl font-semibold cursor-pointer border-b-4 bg-transparent border-b-transparent hover:border-b-stone-200 transform duration-300 w-full text-center"
            @click="scrollToSection('about')"
          >
            About
          </button>
          <button
            class="px-2 py-2 text-xl font-semibold cursor-pointer border-b-4 bg-transparent border-b-transparent hover:border-b-stone-200 transform duration-300 w-full text-center"
            @click="scrollToSection('skills')"
          >
            Skills
          </button>
          <button
            class="px-2 py-2 text-xl font-semibold cursor-pointer border-b-4 bg-transparent border-b-transparent hover:border-b-stone-200 transform duration-300 w-full text-center"
            @click="scrollToSection('resumeNav')"
          >
            Resume
          </button>
          <button
            class="px-2 py-2 text-xl font-semibold cursor-pointer border-b-4 bg-transparent border-b-transparent hover:border-b-stone-200 transform duration-300 w-full text-center"
            @click="scrollToSection('contact')"
          >
            Contact
          </button>
        </div>
      </transition>
    </div>
  </div>
</template>

<style></style>
