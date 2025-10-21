<script lang="ts" setup>
import AnimatedBtn from "@/components/AnimatedBtn.vue";
import { AiCloudDownloadOutlined } from "@twistify/vue3-icons/ai";
import Resume from "@/assets/images/Resume.png";


const downloadResume = () => {
  const link = document.createElement("a");
  link.href = `${import.meta.env.BASE_URL}EmadAp_resume_english.pdf`;
  link.download = "EmadAp_resume_english.pdf";
  link.click();
};

</script>
<template>
  <div
    class="text-center font-main px-4 w-full bg-stone-200 py-20 min-h-screen text-stone-900 overflow-hidden"
  >
    <div
      class="flex flex-col gap-14 lg:gap-20 max-w-screen-2xl py-12 mx-auto items-center"
    >
      <di class="flex flex-col gap-10 lg:gap-16 pb-12 items-center mx-2">
        <h1
        class="underline decoration-solid text-7xl font-semibold font-btn text-center"
      >
          My Resume
        </h1>
        <p class="">
          View my professional qualifications and experience in front-end
          development.
        </p>

        <div
          class="hover:scale-105 mb-24 lg:mb-20 w-full bg-white border border-stone-900/70 shadow-2xl rounded-xl relative transition-all duration-400 inline-flex group"
        >
          <div
            class="absolute rounded-xl transition-all duration-1000 opacity-70 -inset-px bg-gradient-to-r from-sky-300 to-rose-300 via-violet-300 blur-lg group-hover:opacity-100 group-hover:-inset-1 group-hover:duration-200 animate-pulse"
          ></div>
          <img
            class="z-10 mx-auto rounded-xl object-cover"
            :src="Resume"
            alt="resume"
          />
        </div>

        <AnimatedBtn
          label="Download"
          :icon="AiCloudDownloadOutlined"
          :smallRadius="80"
          :bigRadius="110"
          @click="downloadResume"
        />
      </di>
    </div>
  </div>
</template>
<style scoped></style>
