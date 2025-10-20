<script lang="ts" setup>
import AxiosIconSvg from "@/assets/icons/Axios-icon-svg.vue";
import CssIconSvg from "@/assets/icons/Css-icon-svg.vue";
import ExpressIconSvg from "@/assets/icons/Express-icon-svg.vue";
import GithubIconSvg from "@/assets/icons/Github-icon-svg.vue";
import GitlabIconSvg from "@/assets/icons/Gitlab-icon-svg.vue";
import HtmlIconSvg from "@/assets/icons/Html-icon-svg.vue";
import JsIconSvg from "@/assets/icons/Js-icon-svg.vue";
import MaterialUiIconSvg from "@/assets/icons/MaterialUi-icon-svg.vue";
import MongodbIconSvg from "@/assets/icons/Mongodb-icon-svg.vue";
import NextIconSvg from "@/assets/icons/Next-icon-svg.vue";
import NodejsIconSvg from "@/assets/icons/Nodejs-icon-svg.vue";
import ReactIconSvg from "@/assets/icons/React-icon-svg.vue";
import ReactQueryIconSvg from "@/assets/icons/ReactQuery-icon-svg.vue";
import ReduxIconSvg from "@/assets/icons/Redux-icon-svg.vue";
import ShadcnUiIconSvg from "@/assets/icons/ShadcnUi-icon-svg.vue";
import TailwindcssIconSvg from "@/assets/icons/Tailwindcss-icon-svg.vue";
import TsIconSvg from "@/assets/icons/Ts-icon-svg.vue";
import VueIconSvg from "@/assets/icons/Vue-icon-svg.vue";
import AnimatedBtn from "@/components/AnimatedBtn.vue";
import { AiCloudDownloadOutlined } from "@twistify/vue3-icons/ai";
</script>
<template>
  <div
    class="text-center font-main px-4 w-full bg-stone-200 py-20 text-stone-900"
  >
    <div
      class="flex flex-col gap-14 lg:gap-20 max-w-screen-2xl py-12 mx-auto items-center"
    >
      <div class="flex flex-col gap-10 lg:gap-16 pb-12 items-center">
        <h1
          class="underline decoration-solid text-7xl font-semibold font-btn text-center"
        >
          Technical Expertise
        </h1>
        <p class="text-lg md:text-xl xl:text-2xl">
          A refined selection of my proficiency in modern development tools and
          technologies
        </p>
        <div
          class="grid grid-cols-3 lg:grid-cols-6 justify-center gap-x-30 gap-y-20"
        >
          <JsIconSvg />
          <TsIconSvg />
          <MongodbIconSvg />
          <CssIconSvg />
          <HtmlIconSvg />
          <NodejsIconSvg />
          <ReduxIconSvg />
          <VueIconSvg />
          <ExpressIconSvg />
          <GitlabIconSvg />
          <GithubIconSvg />
          <ReactQueryIconSvg />
          <MaterialUiIconSvg />
          <AxiosIconSvg />
          <ShadcnUiIconSvg />
          <ReactIconSvg />
          <TailwindcssIconSvg />
          <NextIconSvg />
        </div>
        <p id="resume" class="text-lg md:text-xl xl:text-2xl">
          Constantly refining and expanding my technical skillset
        </p>
      </div>
      <di class="flex flex-col gap-10 lg:gap-16 pb-12 items-center mx-2">
        <h3
          class="underline decoration-solid text-5xl font-semibold font-btn text-center"
        >
          My Resume
        </h3>
        <p class="">
          View my professional qualifications and experience in front-end
          development.
        </p>

        <div
          class="hover:scale-105 mb-20 w-full bg-white border border-stone-900/70 shadow-2xl rounded-xl relative transition-all duration-400 inline-flex group"
        >
          <div
            class="absolute rounded-xl transition-all duration-1000 opacity-70 -inset-px bg-gradient-to-r from-sky-300 to-rose-300 via-violet-300 blur-lg group-hover:opacity-100 group-hover:-inset-1 group-hover:duration-200 animate-pulse"
          ></div>
          <img
            class="z-10 mx-auto rounded-xl object-cover"
            src="/Resume.png"
            alt="resume"
          />
        </div>

        <AnimatedBtn
          label="Download"
          :icon="AiCloudDownloadOutlined"
          :smallRadius="80"
          :bigRadius="110"
        />
      </di>
    </div>
  </div>
</template>
