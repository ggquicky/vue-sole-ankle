<script setup lang="ts">
import { RouterView } from "vue-router";
import NavBar from "./components/NavBar.vue";
import AdvertisementBanner from "./components/AdvertisementBanner.vue";
</script>

<template>
  <header>
    <AdvertisementBanner />
    <NavBar />
  </header>

  <RouterView />
</template>

<style scoped>
@import "./assets/main.css";
</style>
