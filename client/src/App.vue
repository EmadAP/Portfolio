<script setup lang="ts">
import Mouse from './assets/Mouse.vue';
import Navbar from './template/Navbar.vue';

</script>

<template>
  <div>
    <!-- <nav>
      <router-link to="/">home</router-link
      ><router-link to="/about">about</router-link>
    </nav> -->
    <Navbar />

    <router-view />
    <Mouse />
  </div>
</template>
