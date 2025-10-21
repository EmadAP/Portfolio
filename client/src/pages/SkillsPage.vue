<script lang="ts" setup>
import AxiosIconSvg from "@/components/icons/Axios-icon-svg.vue";
import CssIconSvg from "@/components/icons/Css-icon-svg.vue";
import ExpressIconSvg from "@/components/icons/Express-icon-svg.vue";
import GithubIconSvg from "@/components/icons/Github-icon-svg.vue";
import GitlabIconSvg from "@/components/icons/Gitlab-icon-svg.vue";
import HtmlIconSvg from "@/components/icons/Html-icon-svg.vue";
import JsIconSvg from "@/components/icons/Js-icon-svg.vue";
import MaterialUiIconSvg from "@/components/icons/MaterialUi-icon-svg.vue";
import MongodbIconSvg from "@/components/icons/Mongodb-icon-svg.vue";
import NextIconSvg from "@/components/icons/Next-icon-svg.vue";
import NodejsIconSvg from "@/components/icons/Nodejs-icon-svg.vue";
import ReactIconSvg from "@/components/icons/React-icon-svg.vue";
import ReactQueryIconSvg from "@/components/icons/ReactQuery-icon-svg.vue";
import ReduxIconSvg from "@/components/icons/Redux-icon-svg.vue";
import ShadcnUiIconSvg from "@/components/icons/ShadcnUi-icon-svg.vue";
import TailwindcssIconSvg from "@/components/icons/Tailwindcss-icon-svg.vue";
import TsIconSvg from "@/components/icons/Ts-icon-svg.vue";
import VueIconSvg from "@/components/icons/Vue-icon-svg.vue";
</script>
<template>
  <div
    class="text-center font-main px-4 min-h-screen w-full bg-stone-200 py-20 text-stone-900 overflow-hidden"
  >
    <div
      class="flex flex-col gap-10 lg:gap-16 max-w-screen-2xl py-12 mx-auto pb-12 items-center"
    >
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
        class="grid grid-cols-3 lg:grid-cols-6 justify-center gap-x-15 md:gap-x-30 gap-y-20"
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
  </div>
</template>
