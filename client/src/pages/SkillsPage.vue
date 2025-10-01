<script lang="ts" setup>
import { AiGithubOutlined } from "@twistify/vue3-icons/ai";
import { IonLogoGitlab, IonLogoVue } from "@twistify/vue3-icons/ion";
import {
  MdiLanguageTypescript,
  MdiReact,
  MdiTailwind,
} from "@twistify/vue3-icons/mdi";
import { SkNextjsDark } from "@twistify/vue3-icons/sk";
import { TaBrandJavascript } from "@twistify/vue3-icons/ta";
import { TiCss3, TiHtml5 } from "@twistify/vue3-icons/ti";
</script>
<template>
  <div class="font-main px-4 w-full bg-stone-200 py-12 text-stone-900">
    <div
      class="flex flex-col gap-6 lg:gap-10 max-w-screen-2xl py-12 mx-auto items-center"
    >
      <div class="flex flex-col gap-6 lg:gap-10 pb-12 items-center">
        <h1 class="text-7xl font-semibold font-btn text-center">
          Technical Expertise
        </h1>
        <p class="text-lg md:text-xl xl:text-2xl">
          A refined selection of my proficiency in modern development tools and
          technologies
        </p>
        <div
          class="grid grid-cols-3 md:grid-cols-5 justify-center gap-x-30 gap-y-20"
        >
          <MdiReact size="50" />
          <SkNextjsDark size="50" />
          <TiCss3 size="50" />
          <TiHtml5 size="50" />
          <MdiTailwind size="50" />
          <TaBrandJavascript size="50" />
          <MdiLanguageTypescript size="50" />
          <IonLogoVue size="50" />
          <AiGithubOutlined size="50" />
          <IonLogoGitlab size="50" />
        </div>
        <p class="text-lg md:text-xl xl:text-2xl">
          Constantly refining and expanding my technical skillset
        </p>
      </div>
      <di class="flex flex-col gap-6 lg:gap-10 pb-12 items-center">
        <h3 class="text-5xl font-semibold font-btn text-center">My Resume</h3>
        <p class="">
          View my professional qualifications and experience in front-end
          development.
        </p>
        <div
          class="hover:scale-105 w-full p-1 bg-white border border-stone-900/70 shadow-2xl rounded-xl"
        >
          <img src="/public/Resume.png" alt="resume" />
        </div>
        <button
          class="font-btn bg-stone-800 hover:bg-stone-700 cursor-pointer shadow-2xl text-stone-200 text-2xl px-6 py-2 rounded-xl"
        >
          Download Resume
        </button>
      </di>
    </div>
  </div>
</template>
