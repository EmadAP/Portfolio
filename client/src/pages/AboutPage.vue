<script lang="ts" setup>
import Image from "@/assets/images/image1.jpg";
</script>
<template>
  <div class="font-main px-4 w-full bg-stone-200 py-20 text-stone-900">
    <div
      class="flex flex-col gap-6 lg:gap-10 max-w-screen-2xl py-12 mx-auto items-center"
    >
      <h1
        class="underline decoration-solid text-7xl font-semibold font-btn text-center"
      >
        About me
      </h1>
      <div
        class="h-[350px] w-[350px] rounded-full relative transition-all duration-400 inline-flex group"
      >
        <div
          class="absolute h-[350px] w-[350px] rounded-full transition-all duration-1000 opacity-70 -inset-px bg-gradient-to-r from-sky-300 to-rose-300 via-violet-300 blur-lg group-hover:opacity-100 group-hover:-inset-1 group-hover:duration-200 animate-pulse"
        ></div>
        <img
          class="px-6 py-6 z-10 mx-auto rounded-full object-cover"
          :src="Image"
          alt="developer"
        />
      </div>
      <div class="leading-10 flex flex-col gap-6 pt-8 lg:text-2xl text-xl">
        <p class="">
          I'm a Junior
          <span
            class="bg-stone-900 text-stone-200 text-2xl lg:text-3xl font-semiMain font-extrabold"
            >Front-End Developer</span
          >
          with a passion for building modern, responsive, and user-friendly
          applications. Most of my experience is with React, Next.js,
          TypeScript, React Query, Tailwind CSS, and Shadcn/UI, where I focus on
          creating clean interfaces and smooth user experiences. While my main
          focus is on front-end development, I also have hands-on knowledge of
          Express.js, MongoDB, and Axios, which allows me to build and connect
          simple backends for my own projects. Recently, I’ve been expanding my
          skills by learning Vue, adding another perspective to my development
          toolkit.
        </p>
        <p>
          My journey in development has taught me to balance design and
          functionality—making sure that apps not only look good but also
          perform efficiently and scale well. I enjoy tackling new challenges,
          learning different frameworks, and continuously improving my craft.
          Problem-solving and experimenting with new ideas keep me motivated,
          and I aim to bring clarity and usability to every project I work on.
        </p>
        <p>
          Outside of coding, I like exploring new technologies, keeping up with
          modern web trends, and finding ways to grow as both a developer and a
          creator. Whether I’m building personal projects or experimenting with
          new tools, I’m always excited to learn and push my skills further.
        </p>
      </div>
    </div>
  </div>
</template>
