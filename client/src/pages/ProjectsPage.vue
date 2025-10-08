<script lang="ts" setup>
import AxiosIconSvg from "@/assets/icons/Axios-icon-svg.vue";
import CssIconSvg from "@/assets/icons/Css-icon-svg.vue";
import ExpressIconSvg from "@/assets/icons/Express-icon-svg.vue";
import HtmlIconSvg from "@/assets/icons/Html-icon-svg.vue";
import MongodbIconSvg from "@/assets/icons/Mongodb-icon-svg.vue";
import NextIconSvg from "@/assets/icons/Next-icon-svg.vue";
import NodejsIconSvg from "@/assets/icons/Nodejs-icon-svg.vue";
import ReactIconSvg from "@/assets/icons/React-icon-svg.vue";
import ReactQueryIconSvg from "@/assets/icons/ReactQuery-icon-svg.vue";
import ShadcnUiIconSvg from "@/assets/icons/ShadcnUi-icon-svg.vue";
import TailwindcssIconSvg from "@/assets/icons/Tailwindcss-icon-svg.vue";
import TsIconSvg from "@/assets/icons/Ts-icon-svg.vue";
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
          class="grid grid-cols-1 lg:grid-cols-2 xl:grid-cols-3 items-center justify-between gap-14 w-full"
        >
          <div
            class="relative rounded-2xl lg:col-span-1 xl:col-span-2 h-[500px] mx-auto hover:shadow-2xl transition duration-500"
          >
            <div
              class="p-5 absolute z-10 flex h-[500px] w-full whitespace-normal bg-stone-800 text-center text-stone-200 opacity-0 transition duration-500 rounded-2xl hover:opacity-90"
            >
              <p
                class="md:text-2xl lg:text-lg xl:text-3xl xl:leading-14 lg:leading-12 text-xl font-semibold md:leading-15 leading-10"
              >
                Tickly is a web application I built to make browsing and
                purchasing event tickets easy and intuitive. My goal was to
                create a smooth, interactive user experience, designing a
                frontend that feels responsive and engaging while handling
                real-time data and dynamic content. Through this project, I
                learned how to structure a complete application and bring a
                complex idea to life from concept to a fully functional product.
              </p>
            </div>
            <img
              class="rounded-2xl h-[500px] object-cover mx-auto"
              src="/Tickly.png"
              alt="Tickly-project"
            />
          </div>
          <div
            class="relative lg:col-span-1 xl:col-span-1 h-[500px] bg-stone-100 px-2 py-4 rounded-2xl flex flex-col justify-between gap-4 hover:shadow-2xl transition duration-500"
          >
            <div
              class="hidden lg:flex absolute top-12 -left-7 -translate-y-1/2 w-0 h-0 border-t-[25px] border-t-transparent border-b-[25px] border-b-transparent border-r-[30px] border-r-stone-100 shadow-2xl"
            ></div>
            <div
              class="flex lg:hidden absolute -top-3 left-4 -translate-y-1/2 w-0 h-0 border-l-[25px] border-l-transparent border-b-[25px] border-b-stone-100 border-r-[30px] border-r-transparent shadow-2xl"
            ></div>

            <h1 class="text-4xl font-semibold font-btn">Tech Stack</h1>
            <div class="flex flex-col gap-10">
              <div
                class="flex flex-row justify-between xl:gap-4 2xl:gap-12 gap-12 w-full"
              >
                <h3 class="text-3xl font-btn">Frontend:</h3>
                <div
                  class="w-full grid grid-cols-3 md:grid-cols-5 lg:grid-cols-3 gap-8"
                >
                  <HtmlIconSvg /> <CssIconSvg /> <TsIconSvg />
                  <TailwindcssIconSvg /> <ReactIconSvg /> <NextIconSvg />
                  <ReactQueryIconSvg />
                  <ShadcnUiIconSvg />
                  <AxiosIconSvg />
                </div>
              </div>
              <div
                class="flex flex-row justify-between xl:gap-4 2xl:gap-12 gap-12 w-full"
              >
                <h3 class="text-3xl font-btn">Backend:</h3>
                <div
                  class="w-full grid grid-cols-3 md:grid-cols-5 lg:grid-cols-3 gap-8"
                >
                  <NodejsIconSvg /> <ExpressIconSvg /> <MongodbIconSvg />
                  <AxiosIconSvg />
                </div>
              </div>
            </div>
          </div>
        </div>
        <div
          class="grid grid-cols-1 lg:grid-cols-2 xl:grid-cols-3 items-center justify-between gap-14 w-full"
        >
          <div
            class="relative lg:col-span-1 xl:col-span-1 h-[500px] bg-stone-100 px-2 py-4 rounded-2xl flex flex-col justify-between gap-4 hover:shadow-2xl"
          >
            <div
              class="hidden lg:flex absolute top-12 -right-7 -translate-y-1/2 w-0 h-0 border-t-[25px] border-t-transparent border-b-[25px] border-b-transparent border-l-[30px] border-l-stone-100 shadow-2xl"
            ></div>
            <div
              class="flex lg:hidden absolute -top-3 left-4 -translate-y-1/2 w-0 h-0 border-l-[25px] border-l-transparent border-b-[25px] border-b-stone-100 border-r-[30px] border-r-transparent shadow-2xl"
            ></div>

            <h1 class="text-4xl font-semibold font-btn">Tech Stack</h1>
            <div class="flex flex-col gap-10">
              <div
                class="flex flex-row justify-between xl:gap-4 2xl:gap-12 gap-12 w-full"
              >
                <h3 class="text-3xl font-btn">Frontend:</h3>
                <div
                  class="w-full grid grid-cols-3 md:grid-cols-5 lg:grid-cols-3 gap-8"
                >
                  <HtmlIconSvg /> <CssIconSvg /> <TsIconSvg />
                  <TailwindcssIconSvg /> <ReactIconSvg /> <NextIconSvg />
                  <ReactQueryIconSvg />
                  <ShadcnUiIconSvg />
                  <AxiosIconSvg />
                </div>
              </div>
              <div
                class="flex flex-row justify-between xl:gap-4 2xl:gap-12 gap-12 w-full"
              >
                <h3 class="text-3xl font-btn">Backend:</h3>
                <div
                  class="w-full grid grid-cols-3 md:grid-cols-5 lg:grid-cols-3 gap-8"
                >
                  <NodejsIconSvg /> <ExpressIconSvg /> <MongodbIconSvg />
                  <AxiosIconSvg />
                </div>
              </div>
            </div>
          </div>
          <div
            class="relative rounded-2xl lg:col-span-1 xl:col-span-2 h-[500px] mx-auto hover:shadow-2xl transition duration-500"
          >
            <div
              class="p-5 absolute z-10 flex h-[500px] w-full whitespace-normal bg-stone-800 text-center text-stone-200 opacity-0 transition duration-500 rounded-2xl hover:opacity-90"
            >
              <p
                class="md:text-2xl lg:text-lg xl:text-3xl xl:leading-14 lg:leading-12 text-xl font-semibold md:leading-15 leading-10"
              >
                The Tickly Dashboard was built as the admin side of the
                platform, giving organizers the ability to manage events,
                tickets, and sales in one place. My goal with this part of the
                project was to create a clear and efficient interface that makes
                complex data easy to understand and control. Building it taught
                me how to design for usability and scalability, while connecting
                the frontend seamlessly with backend operations.
              </p>
            </div>
            <img
              class="rounded-2xl h-[500px] object-cover mx-auto"
              src="/Tickly-Dashboard.png"
              alt="Tickly-Dashboard-project"
            />
          </div>
        </div>
        <div
          class="grid grid-cols-1 lg:grid-cols-2 xl:grid-cols-3 items-center justify-between gap-14 w-full"
        >
          <div
            class="relative rounded-2xl lg:col-span-1 xl:col-span-2 h-[500px] mx-auto hover:shadow-2xl transition duration-500"
          >
            <div
              class="p-5 absolute z-10 flex h-[500px] w-full whitespace-normal bg-stone-800 text-center text-stone-200 opacity-0 transition duration-500 rounded-2xl hover:opacity-90"
            >
              <p
                class="md:text-2xl lg:text-lg xl:text-3xl xl:leading-14 lg:leading-12 text-xl font-semibold md:leading-15 leading-10"
              >
                StayNest is a web application I built to let users list and
                explore properties for short-term stays. My goal was to create a
                smooth listing and browsing experience, where users can easily
                post their own properties and discover others. Through this
                project, I focused on building a responsive, user-friendly
                interface and handling dynamic data in a way that feels seamless
                and reliable.
              </p>
            </div>
            <img
              class="rounded-2xl h-[500px] object-cover mx-auto"
              src="/Staynest.png"
              alt="StayNest-project"
            />
          </div>
          <div
            class="relative lg:col-span-1 xl:col-span-1 h-[500px] bg-stone-100 px-2 py-4 rounded-2xl flex flex-col justify-between gap-4 hover:shadow-2xl transition duration-500"
          >
            <div
              class="hidden lg:flex absolute top-12 -left-7 -translate-y-1/2 w-0 h-0 border-t-[25px] border-t-transparent border-b-[25px] border-b-transparent border-r-[30px] border-r-stone-100 shadow-2xl"
            ></div>
            <div
              class="flex lg:hidden absolute -top-3 left-4 -translate-y-1/2 w-0 h-0 border-l-[25px] border-l-transparent border-b-[25px] border-b-stone-100 border-r-[30px] border-r-transparent shadow-2xl"
            ></div>

            <h1 class="text-4xl font-semibold font-btn">Tech Stack</h1>
            <div class="flex flex-col gap-10">
              <div
                class="flex flex-row justify-between xl:gap-4 2xl:gap-12 gap-12 w-full"
              >
                <h3 class="text-3xl font-btn">Frontend:</h3>
                <div
                  class="w-full grid grid-cols-3 md:grid-cols-5 lg:grid-cols-3 gap-8"
                >
                  <HtmlIconSvg /> <CssIconSvg /> <TsIconSvg />
                  <TailwindcssIconSvg /> <ReactIconSvg /> <NextIconSvg />
                  <ShadcnUiIconSvg />
                </div>
              </div>
              <div
                class="flex flex-row justify-between xl:gap-4 2xl:gap-12 gap-12 w-full"
              >
                <h3 class="text-3xl font-btn">Backend:</h3>
                <div
                  class="w-full grid grid-cols-3 md:grid-cols-5 lg:grid-cols-3 gap-8"
                >
                  <NodejsIconSvg /> <ExpressIconSvg /> <MongodbIconSvg />
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
