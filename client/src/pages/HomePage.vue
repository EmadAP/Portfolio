<script setup lang="ts">
function scrollToSection(id: string) {
  const el = document.getElementById(id);
  if (el) {
    el.scrollIntoView({ behavior: "smooth" });
  }
}
</script>
<template>
  <div class="font-main bg-stone-200 text-stone-900 h-screen">
    <div
      class="pt-30 pb-10 gap-10 h-full px-3 lg:px-20 flex flex-col items-center justify-around text-center max-w-screen-2xl mx-auto"
    >
      <h1
        class="relative font-title text-6xl sm:text-7xl md:text-8xl font-bold w-fit"
      >
        <span>Hi!. My name is Emad Amoupour</span>
      </h1>

      <p class="md:text-2xl lg:text-3xl text-xl md:leading-16 leading-12">
        <span class="font-semiMain font-extrabold lg:text-4xl text-3xl"
          >Welcome to my portfolio.
        </span>
        I’m a Junior
        <span class="font-semiMain bg-stone-800 text-stone-200"
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
        <button
          class="hover:scale-105 duration-300 bg-stone-800 hover:bg-stone-700 cursor-pointer shadow-2xl text-stone-200 text-2xl px-6 py-2 rounded-xl"
          @click="scrollToSection('resume')"
        >
          Resume
        </button>

        <button
          class="hover:scale-105 duration-300 bg-stone-800 hover:bg-stone-700 cursor-pointer shadow-2xl text-stone-200 text-2xl px-6 py-2 rounded-xl"
          @click="scrollToSection('contact')"
        >
          Contact
        </button>
      </div>
    </div>
  </div>
</template>

<style scoped></style>
