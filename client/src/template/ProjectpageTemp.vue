<script setup lang="ts">
import PaperClipIconSvg from "@/assets/icons/PaperClip-icon-svg.vue";
import MagneticWrapper from "@/components/MagneticWrapper.vue"; // adjust this import based on your structure

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
  <div class="flex flex-col items-center justify-between gap-14 w-full">
    <!-- Project Image with Hover Overlay -->
    <a
      :href="repoUrl"
      target="_blank"
      rel="noopener noreferrer"
      class="relative rounded-2xl lg:col-span-2 h-[600px] w-full mx-auto hover:shadow-2xl transition duration-500"
    >
      <div
        class="p-5 absolute z-10 flex h-[600px] w-full whitespace-normal bg-stone-800 text-center text-stone-200 opacity-0 transition duration-500 rounded-2xl hover:opacity-90"
      >
        <p
          class="font-semibold text-xl leading-10 sm:text-3xl sm:leading-13 md:text-4xl lg:leading-16 xl:leading-20 2xl:text-5xl"
        >
          <span
            class="font-semiMain text-3xl md:text-5xl xl:text-5 xl text-stone-800 bg-stone-200"
          >
            {{ projectName }}
          </span>
          {{ description }}
        </p>
      </div>
      <img
        class="rounded-2xl h-[600px] w-full object-contain mx-auto bg-stone-100"
        :src="imageUrl"
        :alt="`${projectName}-project`"
      />
    </a>

    <!-- Frontend / Backend Cards -->
    <div
      class="flex flex-col lg:flex-row justify-around w-full gap-4 lg:gap-10"
    >
      <MagneticWrapper :strength="100" :range="400">
        <div
          class="relative h-fit lg:w-fit bg-stone-100 px-2 py-10 rounded-2xl flex flex-col gap-8 hover:shadow-2xl transition duration-500"
        >
          <div class="flex absolute -top-6 right-6">
            <PaperClipIconSvg />
          </div>
          <div class="flex flex-col gap-8 w-full">
            <h3 class="text-5xl font-bold font-btn">{{ frontend.name }}:</h3>
            <div class="w-full border-b-3 border-dashed"></div>
            <div class="w-full grid grid-cols-5 gap-8 lg:gap-12">
              <component
                v-for="(icon, index) in frontend.icons"
                :is="icon"
                :key="index"
              />
            </div>
          </div>
        </div>
      </MagneticWrapper>

      <MagneticWrapper :strength="100" :range="400">
        <div
          class="relative h-fit lg:w-fit bg-stone-100 px-2 py-10 rounded-2xl flex flex-col gap-8 hover:shadow-2xl transition duration-500"
        >
          <div class="hidden lg:flex absolute -top-6 right-6">
            <PaperClipIconSvg />
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
            <div
              class="w-full grid grid-cols-5 lg:grid-cols-4 gap-8 lg:gap-12"
            >
              <component
                v-for="(icon, index) in backend.icons"
                :is="icon"
                :key="index"
              />
            </div>
          </div>
        </div>
      </MagneticWrapper>
    </div>
  </div>
</template>
