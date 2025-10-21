<script lang="ts" setup>
import AxiosIconSvg from "@/components/icons/Axios-icon-svg.vue";
import CssIconSvg from "@/components/icons/Css-icon-svg.vue";
import ExpressIconSvg from "@/components/icons/Express-icon-svg.vue";
import HtmlIconSvg from "@/components/icons/Html-icon-svg.vue";
import MongodbIconSvg from "@/components/icons/Mongodb-icon-svg.vue";
import NextIconSvg from "@/components/icons/Next-icon-svg.vue";
import NodejsIconSvg from "@/components/icons/Nodejs-icon-svg.vue";
import ReactIconSvg from "@/components/icons/React-icon-svg.vue";
import ReactQueryIconSvg from "@/components/icons/ReactQuery-icon-svg.vue";
import ShadcnUiIconSvg from "@/components/icons/ShadcnUi-icon-svg.vue";
import TailwindcssIconSvg from "@/components/icons/Tailwindcss-icon-svg.vue";
import TsIconSvg from "@/components/icons/Ts-icon-svg.vue";
import MovingText from "@/components/MovingText.vue";
import ProjectPageTemp from "@/template/ProjectPageTemp.vue";
import Tickly from "@/assets/images/Tickly.png";
import TicklyDashboard from "@/assets/images/Tickly-Dashboard.png";
import StayNest from "@/assets/images/Staynest.png";
</script>
<template>
  <div class="font-main w-full bg-stone-200 text-stone-900 py-20">
    <div class="w-full h-full py-12 items-center">
      <h1
        class="max-w-screen-2xl mx-auto underline decoration-solid md:text-7xl text-5xl font-semibold font-btn text-center"
      >
        Projects
      </h1>

      <div
        class="pt-20 flex flex-col items-center h-full justify-between gap-30"
      >
        <ProjectPageTemp
          projectName="Tickly"
          repoUrl="https://github.com/EmadAP/Tickly/tree/main/client"
          :imageUrl="Tickly"
          description="is a web application I built to make browsing and purchasing
                event tickets easy and intuitive. My goal was to create a
                smooth, interactive user experience, designing a frontend that
                feels responsive and engaging while handling real-time data and
                dynamic content. Through this project, I learned how to
                structure a complete application and bring a complex idea to
                life from concept to a fully functional product."
          :frontend="{
            name: 'Frontend',
            icons: [
              HtmlIconSvg,
              CssIconSvg,
              TsIconSvg,
              TailwindcssIconSvg,
              ReactIconSvg,
              NextIconSvg,
              ReactQueryIconSvg,
              AxiosIconSvg,
            ],
          }"
          :backend="{
            name: 'Backend',
            icons: [
              NodejsIconSvg,
              ExpressIconSvg,
              MongodbIconSvg,
              AxiosIconSvg,
            ],
          }"
        />
        <MovingText />
        <ProjectPageTemp
          projectName="Tickly Dashboard"
          repoUrl="https://github.com/EmadAP/Tickly/tree/main/admin"
          :imageUrl="TicklyDashboard"
          description=" was built as the admin side of the platform, giving organizers
                the ability to manage events, tickets, and sales in one place.
                My goal with this part of the project was to create a clear and
                efficient interface that makes complex data easy to understand
                and control. Building it taught me how to design for usability
                and scalability, while connecting the frontend seamlessly with
                backend operations."
          :frontend="{
            name: 'Frontend',
            icons: [
              HtmlIconSvg,
              CssIconSvg,
              TsIconSvg,
              TailwindcssIconSvg,
              ReactIconSvg,
              NextIconSvg,
              ReactQueryIconSvg,
              AxiosIconSvg,
            ],
          }"
          :backend="{
            name: 'Backend',
            icons: [
              NodejsIconSvg,
              ExpressIconSvg,
              MongodbIconSvg,
              AxiosIconSvg,
            ],
          }"
        />
        <MovingText />
        <ProjectPageTemp
          projectName="StayNest"
          repoUrl="https://github.com/EmadAP/StayNest"
          :imageUrl="StayNest"
          description="is a web application I built to let users list and explore
                properties for short-term stays. My goal was to create a smooth
                listing and browsing experience, where users can easily post
                their own properties and discover others. Through this project,
                I focused on building a responsive, user-friendly interface and
                handling dynamic data in a way that feels seamless and reliable."
          :frontend="{
            name: 'Frontend',
            icons: [
              HtmlIconSvg,
              CssIconSvg,
              TsIconSvg,
              TailwindcssIconSvg,
              ReactIconSvg,
              NextIconSvg,
              ShadcnUiIconSvg,
            ],
          }"
          :backend="{
            name: 'Backend',
            icons: [
              NodejsIconSvg,
              ExpressIconSvg,
              MongodbIconSvg,
              AxiosIconSvg,
            ],
          }"
        />
      </div>
    </div>
  </div>
</template>
