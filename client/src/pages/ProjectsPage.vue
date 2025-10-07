<script lang="ts" setup>
import { Music } from "lucide-vue-next";
</script>
<template>
  <div class="font-main px-4 w-full bg-stone-200 py-20 text-stone-900">
    <div class="max-w-screen-2xl h-full py-12 mx-auto items-center">
      <h1 class="md:text-7xl text-5xl font-semibold font-btn text-center">
        Projects
      </h1>
      <div
        class="pt-20 flex flex-col items-center h-full justify-between gap-20"
      >
        <div
          class="grid grid-cols-1 lg:grid-cols-2 items-center justify-between gap-20 w-full"
        >
          <img
            class="rounded-2xl h-[400px] object-cover mx-auto"
            src="/public/Cat-on-couch.jpg"
            alt="cat"
          />
          <div class="w-full py-6">
            <h1 class="text-4xl font-semibold pb-18">Tech Stack</h1>
            <div class="flex flex-col justify-between gap-20">
              <div class="flex flex-row justify-between gap-12 w-full">
                <h3 class="text-3xl">Frontend:</h3>
                <div class="w-full grid grid-cols-6 gap-4">
                  <Music /><Music /><Music /><Music /><Music /><Music /><Music />
                </div>
              </div>
              <div class="flex flex-row justify-between gap-12 w-full">
                <h3 class="text-3xl">Backend:</h3>
                <div class="w-full grid grid-cols-6 gap-4">
                  <Music /><Music /><Music /><Music /><Music /><Music /><Music />
                </div>
              </div>
            </div>
          </div>
        </div>
        <div
          class="grid grid-cols-1 lg:grid-cols-2 items-center justify-between gap-20 w-full"
        >
          <img
            class="rounded-2xl h-[400px] object-cover mx-auto"
            src="/public/Cat-on-couch.jpg"
            alt="cat"
          />
          <div class="w-full py-6">
            <h1 class="text-4xl font-semibold pb-18">Tech Stack</h1>
            <div class="flex flex-col justify-between gap-20">
              <div class="flex flex-row justify-between gap-12 w-full">
                <h3 class="text-3xl">Frontend:</h3>
                <div class="w-full grid grid-cols-6 gap-4">
                  <Music /><Music /><Music /><Music /><Music /><Music /><Music />
                </div>
              </div>
              <div class="flex flex-row justify-between gap-12 w-full">
                <h3 class="text-3xl">Backend:</h3>
                <div class="w-full grid grid-cols-6 gap-4">
                  <Music /><Music /><Music /><Music /><Music /><Music /><Music />
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
