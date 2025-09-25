<script setup lang="ts">
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
  </div>
</template>
