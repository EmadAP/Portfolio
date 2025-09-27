<script lang="ts" setup>
import { RaHamburgerMenu } from "@twistify/react-icons/ra";
import { ChevronLeft, ChevronRight, Menu, Slash } from "lucide-vue-next";
</script>
<template>
  <div
    class="font-btn sticky z-20 inset-x-0 top-0 px-4 w-full h-20 bg-stone-800"
  >
    <div
      class="flex flex-row justify-between max-w-screen-2xl mx-auto text-white items-center h-full"
    >
      <button class="cursor-pointer">
        <div class="flex flex-row items-center">
          <ChevronLeft />
          <p class="text-3xl font-base">Emad Amoupour</p>
          <Slash class="-rotate-[20deg]" />
          <ChevronRight />
        </div>
      </button>
      <div class="md:flex hidden flex-row items-center justify-center gap-6">
        <button class="Nav-Btn">Home</button>
        <button class="Nav-Btn">Projects</button>
        <button class="Nav-Btn">About</button>
        <button class="Nav-Btn">Contact</button>
      </div>
      <div class="md:hidden flex">
        <Menu />
      </div>
    </div>
  </div>
</template>

<style scoped>
.Nav-Btn {
  padding: 6px 12px;
  font-size: 20px;
  font-weight: 550;
  cursor: pointer;
  border-radius: 8px;
}
.Nav-Btn:hover {
  background-color: oklch(37.4% 0.01 67.558);
}
</style>
