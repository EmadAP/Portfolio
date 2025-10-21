<script lang="ts" setup>
import { AiPhoneOutlined } from "@twistify/vue3-icons/ai";
import { IonEmail } from "@twistify/vue3-icons/ion";
import { TiLocation } from "@twistify/vue3-icons/ti";
import { AiGithubFilled } from "@twistify/vue3-icons/ai";
import { MdiTelegram } from "@twistify/vue3-icons/mdi";
import { RaLinkedinLogo } from "@twistify/vue3-icons/ra";
import { AiLinkOutlined } from "@twistify/vue3-icons/ai";
import { LuClipboardCopy } from "@twistify/vue3-icons/lu";
const copyEmail = () => {
  navigator.clipboard.writeText("Emad.amoupour1997@gmail.com");
};
const copyPhone = () => {
  navigator.clipboard.writeText("+98 911 886 0294");
};
</script>
<template>
  <div class="font-main bg-stone-200 min-h-screen py-20 text-stone-900 ">
    <div
      class="h-full py-14 md:py-16 px-6 lg:px-20 flex flex-col gap-14 items-center justify-between max-w-screen-2xl mx-auto"
    >
      <h1
        class="underline decoration-solid text-7xl font-semibold font-btn text-center"
      >
        Contact me
      </h1>
      <p class="text-xl text-center">
        I'm always happy to discuss opportunities, answer questions, or explore
        new ideas. Send a message or connect online.
      </p>
      <div
        class="w-full grid grid-cols-1 lg:grid-cols-2 justify-between gap-8 border py-10 px-5 rounded-xl shadow-2xl hover:scale-105 duration-300 bg-stone-100"
      >
        <div class="flex flex-col gap-8">
          <h3 class="font-btn font-semibold text-start text-3xl pb-5">
            Contact Information
          </h3>

          <div class="flex flex-row gap-4">
            <IonEmail :size="50" />
            <div class="flex flex-col gap-2 items-start">
              <h3 class="font-semibold text-base">Email</h3>
              <span
                class="text-sm text-stone-700 cursor-pointer flex flex-row items-center gap-2"
                @click="copyEmail"
                >Emad.amoupour1997@gmail.com<LuClipboardCopy
              /></span>
            </div>
          </div>
          <div class="flex flex-row gap-4">
            <AiPhoneOutlined :size="50" />
            <div class="flex flex-col gap-2 items-start">
              <h3 class="font-semibold text-base">Phone</h3>
              <span
                class="text-sm text-stone-700 cursor-pointer flex flex-row items-center gap-2"
                @click="copyPhone"
                >+98 911 886 0294<LuClipboardCopy
              /></span>
            </div>
          </div>
          <div class="flex flex-row gap-4">
            <AiGithubFilled :size="50" />
            <div class="flex flex-col gap-2 items-start">
              <h3 class="font-semibold text-base">Github</h3>
              <a
                href="https://github.com/EmadAP"
                target="_blank"
                class="text-sm text-stone-700 flex flex-row gap-2 items-center"
                >github.com/EmadAP <AiLinkOutlined
              /></a>
            </div>
          </div>
          <div class="flex flex-row gap-4">
            <RaLinkedinLogo :size="50" />
            <div class="flex flex-col gap-2 items-start">
              <h3 class="font-semibold text-base">Linkedin</h3>
              <a
                href="https://www.linkedin.com/in/emad-amoupour-60983438b/"
                target="_blank"
                class="text-sm text-stone-700 flex flex-row gap-2 items-center"
                >linkedin.com/emad-amoupour <AiLinkOutlined
              /></a>
            </div>
          </div>
          <div class="flex flex-row gap-4">
            <MdiTelegram :size="50" />
            <div class="flex flex-col gap-2 items-start">
              <h3 class="font-semibold text-base">Telegram</h3>

              <a
                href="https://t.me/EmadAP"
                target="_blank"
                class="text-sm text-stone-700 flex flex-row gap-2 items-center"
                >t.me/EmadAP <AiLinkOutlined
              /></a>
            </div>
          </div>
          <div class="flex flex-row gap-4">
            <TiLocation :size="50" />
            <div class="flex flex-col gap-2 items-start">
              <h3 class="font-semibold text-base">Location</h3>
              <span class="text-sm text-stone-700">Iran-Gilan</span>
            </div>
          </div>
        </div>
        <div class="flex flex-col gap-8">
          <h3 class="font-btn font-semibold text-start text-3xl pb-5">
            Send me a message
          </h3>

          <div class="flex flex-col gap-2">
            <label for="name">Your Name</label>
            <div
              class="rounded-xl relative transition-all duration-400 inline-flex group"
            >
              <div
                class="absolute rounded-xl transition-all duration-1000 opacity-90 -inset-px bg-gradient-to-r from-sky-400 to-rose-400 via-violet-400 blur-lg group-hover:opacity-100 group-hover:-inset-1 group-hover:duration-200 animate-pulse"
              ></div>
              <input
                type="text"
                id="name"
                placeholder="What's your name?"
                class="border outline-none bg-stone-200 py-3 px-2 rounded-xl z-10 w-full"
              />
            </div>
          </div>

          <div class="flex flex-col gap-2">
            <label for="email">Your Email</label>
            <div
              class="rounded-xl relative transition-all duration-400 inline-flex group"
            >
              <div
                class="absolute rounded-xl transition-all duration-1000 opacity-90 -inset-px bg-gradient-to-r from-sky-400 to-rose-400 via-violet-400 blur-lg group-hover:opacity-100 group-hover:-inset-1 group-hover:duration-200 animate-pulse"
              ></div>
              <input
                type="email"
                id="email"
                placeholder="What's your email?"
                class="border outline-none bg-stone-200 py-3 px-2 rounded-xl z-10 w-full"
              />
            </div>
          </div>
          <div class="flex flex-col gap-2">
            <label for="msg">Your message</label>
            <div
              class="rounded-xl relative transition-all duration-400 inline-flex group"
            >
              <div
                class="absolute rounded-xl transition-all duration-1000 opacity-90 -inset-px bg-gradient-to-r from-sky-400 to-rose-400 via-violet-400 blur-lg group-hover:opacity-100 group-hover:-inset-1 group-hover:duration-200 animate-pulse"
              ></div>

              <textarea
                type="text"
                cols="20"
                rows="5"
                id="msg"
                placeholder="What would you like to say?"
                class="border outline-none bg-stone-200 py-3 px-2 rounded-xl z-10 w-full"
              ></textarea>
            </div>
          </div>
          <button
            class="font-btn bg-gradient-to-r from-sky-300 to-rose-300 via-violet-300 gradient element-to-rotate duration-300 cursor-pointer shadow-2xl text-stone-200 text-2xl px-6 py-2 rounded-xl"
          >
            Send Message
          </button>
        </div>
      </div>
    </div>
  </div>
</template>
<style scoped>
@keyframes gradientChange {
  0% {
    background-position: 0%;
  }

  50% {
    background-position: 100%;
  }

  100% {
    background-position: 0%;
  }
}

.gradient {
  background: linear-gradient(
    90deg,
    oklch(82.8% 0.111 230.318),
    oklch(81.1% 0.111 293.571),
    oklch(81% 0.117 11.638)
  );
  background-size: 200% 200%;
}

.element-to-rotate {
  animation: gradientChange 6s ease infinite;
}
</style>
