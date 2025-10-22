<script setup lang="ts">
import PaperClipper from "@/assets/images/PaperClipper.png";
interface TechStack {
  name: string;
  icons: any[];
}

interface Props {
  projectName: string;
  repoUrl: string;
  imageUrl: string;
  description: string;
  frontend: TechStack;
  backend: TechStack;
}

const props = defineProps<Props>();
</script>

<template>
  <div
    class="grid grid-cols-1 2xl:grid-cols-4 xl:items-center justify-between gap-10 w-full xl:px-20 sm:px-8 px-2"
  >
    <a
      :href="repoUrl"
      target="_blank"
      rel="noopener noreferrer"
      class="group col-span-1 2xl:col-span-3 relative rounded-2xl h-fit w-full mx-auto transition-all duration-500"
    >
      <div
        class="spinColor gradient element-to-rotate shadow-2xl absolute z-0 rounded-2xl transition-all duration-1000 opacity-70 -inset-px bg-gradient-to-r from-sky-400 to-rose-400 via-violet-400 blur-lg group-hover:opacity-100 group-hover:-inset-1 group-hover:duration-200 animate-pulse"
      ></div>
      <div class="relative z-10 m-5">
        <div
          class="hidden lg:flex p-5 absolute z-10 h-full w-full whitespace-normal bg-stone-800 text-center text-stone-200 opacity-0 transition duration-500 rounded-2xl hover:opacity-90"
        >
          <p
            class="font-semibold lg:leading-16 lg:text-2xl xl:text-3xl xl:leading-20 2xl:text-3xl 2xl:leading-16 my-auto"
          >
            <span
              class="font-semiMain lg:text-3xl xl:text-5xl text-stone-800 bg-stone-200"
            >
              {{ projectName }}
            </span>
            {{ description }}
          </p>
        </div>
        <img
          class="rounded-t-2xl lg:rounded-2xl h-fit w-fit object-contain mx-auto bg-stone-100"
          :src="imageUrl"
          :alt="`${projectName}-project`"
        />
        <div
          class="rounded-b-2xl flex lg:hidden px-2 sm:px-5 py-10 h-full w-full whitespace-normal bg-stone-200 text-start sm:text-center text-stone-900"
        >
          <p
            class="sm:font-semibold text-lg leading-10 sm:text-2xl sm:leading-13 md:text-2xl"
          >
            <span
              class="font-semiMain text-xl sm:text-3xl text-stone-200 bg-stone-900"
            >
              {{ projectName }}
            </span>
            {{ description }}
          </p>
        </div>
      </div>
    </a>

    <div
      class="col-span-1 2xl:col-span-1 flex flex-col lg:flex-row 2xl:flex-col justify-around w-full gap-4 lg:gap-10"
    >
      <div
        class="relative h-fit xl:w-fit bg-stone-100 px-2 py-10 rounded-2xl flex flex-col gap-8 hover:shadow-2xl transition duration-500"
      >
        <div class="flex absolute -top-5 right-5">
          <img :src="PaperClipper" alt="clipper" />
        </div>
        <div class="flex flex-col gap-8 w-full">
          <h3 class="text-5xl font-bold font-btn">{{ frontend.name }}:</h3>
          <div class="w-full border-b-3 border-dashed"></div>
          <div class="w-full grid grid-cols-4 gap-8 lg:gap-12">
            <component
              v-for="(icon, index) in frontend.icons"
              :is="icon"
              :key="index"
            />
          </div>
        </div>
      </div>

      <div
        class="relative h-fit xl:w-fit bg-stone-100 px-2 py-10 rounded-2xl flex flex-col gap-8 hover:shadow-2xl transition duration-500"
      >
        <div class="hidden lg:flex absolute -top-5 right-5">
          <img :src="PaperClipper" alt="clipper" />
        </div>
        <div
          class="flex flex-row lg:hidden absolute -top-8 left-1/2 -translate-x-1/2 justify-between w-full gap-2"
        >
          <div
            class="flex flex-row absolute -top-1 left-8 -translate-x-1/2 items-center gap-2"
          >
            <div class="w-2 h-13 bg-stone-800 rounded-full"></div>
            <div class="w-2 h-13 bg-stone-800 rounded-full"></div>
          </div>
          <div
            class="flex flex-row absolute -top-1 right-3 -translate-x-1/2 items-center gap-2"
          >
            <div class="w-2 h-13 bg-stone-800 rounded-full"></div>
            <div class="w-2 h-13 bg-stone-800 rounded-full"></div>
          </div>
        </div>
        <div class="flex flex-col gap-8 w-full">
          <h3 class="text-5xl font-bold font-btn">{{ backend.name }}:</h3>
          <div class="w-full border-b-3 border-dashed"></div>
          <div class="w-full grid grid-cols-4 gap-8 lg:gap-12">
            <component
              v-for="(icon, index) in backend.icons"
              :is="icon"
              :key="index"
            />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
