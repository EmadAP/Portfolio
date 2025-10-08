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
</script>
<template>
  <div class="font-main px-4 w-full bg-stone-200 py-20 text-stone-900">
    <div
      class="flex flex-col gap-14 lg:gap-20 max-w-screen-2xl py-12 mx-auto items-center"
    >
      <div class="flex flex-col gap-10 lg:gap-16 pb-12 items-center">
        <h1 class="text-7xl font-semibold font-btn text-center">
          Technical Expertise
        </h1>
        <p class="text-lg md:text-xl xl:text-2xl">
          A refined selection of my proficiency in modern development tools and
          technologies
        </p>
        <div
          class="grid grid-cols-3 md:grid-cols-6 justify-center gap-x-30 gap-y-20"
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
      <di class="flex flex-col gap-10 lg:gap-16 pb-12 items-center">
        <h3 class="text-5xl font-semibold font-btn text-center">My Resume</h3>
        <p class="">
          View my professional qualifications and experience in front-end
          development.
        </p>
        <div
          class="hover:scale-105 duration-300 w-full p-1 bg-white border border-stone-900/70 shadow-2xl rounded-xl"
        >
          <img src="/public/Resume.png" alt="resume" />
        </div>
        <button
          class="font-btn hover:scale-105 duration-300 bg-stone-800 hover:bg-stone-700 cursor-pointer shadow-2xl text-stone-200 text-2xl px-6 py-2 rounded-xl"
        >
          Download Resume
        </button>
      </di>
    </div>
  </div>
</template>
