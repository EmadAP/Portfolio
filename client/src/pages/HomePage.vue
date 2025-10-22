<script setup lang="ts">
import AnimatedBtn from "@/components/AnimatedBtn.vue";
import { MiResume } from "@twistify/vue3-icons/mi";
import { IonMdContact } from "@twistify/vue3-icons/ion";

function scrollToSection(id: string) {
  const el = document.getElementById(id);
  if (el) {
    el.scrollIntoView({ behavior: "smooth" });
  }
}
</script>
<template>
  <div
    class="text-center font-main px-2 sm:px-4 min-h-screen w-full bg-stone-200 my-auto py-20 text-stone-900 overflow-hidden"
  >
    <div
      class="pb-20 pt-20 md:pt-32 2xl:pt-40 gap-20 h-full px-3 lg:px-20 flex flex-col items-center justify-between text-center max-w-screen-2xl mx-auto"
    >
      <h1
        class="pb-10 md:pb-0 font-btn sm:w-fit flex flex-col md:flex-row items-start md:items-center gap-4 lg:gap-2 w-full"
      >
        <span
          class="text-2xl sm:text-3xl md:text-5xl md:font-black lg:text-6xl xl:text-7xl 2xl:text-8xl font-bold pl-1"
          >Hi!. My name is , </span
        ><span
          class="text-4xl leading-16 sm:leading-[70px] sm:text-7xl md:text-5xl md:font-black lg:text-6xl xl:text-7xl 2xl:text-8xl font-bold"
          >Emad Amoupour</span
        >
      </h1>

      <p
        class="pb-6 text-start sm:text-center md:text-2xl xl:text-3xl text-lg sm:text-xl md:leading-13 lg:leading-16 leading-11"
      >
        <span
          class="font-semiMain font-black lg:text-3xl xl:text-4 text-xl sm:text-2xl"
          >Welcome to my portfolio.
        </span>
        I’m a Junior
        <span class="font-semiMain font-extrabold bg-stone-800 text-stone-200"
          >Front-End Developer</span
        >
        passionate about building responsive, user-friendly interfaces and
        bringing designs to life with clean and modern code. I focus on crafting
        intuitive experiences that work seamlessly across devices, while also
        exploring the backend side to understand the full picture of web
        development. Alongside coding, I enjoy learning new tools, experimenting
        with creative ideas, and continuously improving my skills to grow as a
        developer.
      </p>

      <div class="font-btn flex flex-row items-center justify-around w-full">
        <AnimatedBtn
          label="Resume"
          :icon="MiResume"
          :smallRadius="63"
          :bigRadius="78"
          @click="scrollToSection('resume')"
        />

        <AnimatedBtn
          label="Contact"
          :icon="IonMdContact"
          :smallRadius="65"
          :bigRadius="83"
          @click="scrollToSection('contact')"
        />
      </div>
    </div>
  </div>
</template>

<style scoped></style>
