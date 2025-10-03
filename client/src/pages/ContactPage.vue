<script lang="ts" setup>
import { IonEmail } from "@twistify/vue3-icons/ion";
import { MiContactPage } from "@twistify/vue3-icons/mi";
</script>
<template>
  <div class="font-main bg-stone-200 h-[93vh] text-stone-900">
    <div
      class="h-full py-16 md:py-20 px-3 lg:px-20 flex flex-col gap-16 items-center justify-around text-center max-w-screen-2xl mx-auto"
    >
      <h1 class="text-7xl font-semibold font-btn text-center">Contact me</h1>
      <p class="text-xl">
        I'm always happy to discuss opportunities, answer questions, or explore
        new ideas. Send a message or connect online.
      </p>
      <div class="grid grid-cols-1 lg:grid-cols-2 justify-between gap-8">
        <div class="flex flex-col gap-8">
          <div class="flex flex-row gap-4 items-center">
            <MiContactPage :size="70" />
            <div class="flex flex-col gap-4 items-start">
              <h3 class="font-btn font-semibold text-xl">
                Contact Information
              </h3>
              <span class="text-sm text-stone-700"
                >Reach me directly via email or phone for questions or
                collaborations.</span
              >
            </div>
          </div>
          <div class="flex flex-row gap-4   items-baseline">
            <IonEmail :size="40" class="" />
            <div class="flex flex-col gap-2 items-start">
              <h3 class="font-semibold text-base">Email</h3>
              <span class="text-sm text-stone-700"
                >Emad.amoupour1997@gmail.com</span
              >
            </div>
          </div>
          <AiPhoneOutlined />
        </div>
        <div class="flex flex-col gap-8">
          <div></div>
        </div>
      </div>
    </div>
  </div>
</template>
