<script setup lang="ts">
const sideItems = [
  { name: "Lifestyle" },
  { name: "Jordan" },
  { name: "Running" },
  { name: "Basketball" },
  { name: "Training & Gym" },
  { name: "Football" },
  { name: "Skateboarding" },
  { name: "American Football" },
  { name: "Baseball" },
  { name: "Golf" },
  { name: "Tennis" },
  { name: "Athletics" },
  { name: "Walking" },
];
</script>

<template>
  <div class="flex flex-col gap-y-[40px]">
    <div class="flex gap-3 lg:mt-2">
      <a class="text-base">Home</a>
      <p>/</p>
      <a>Sales</a>
      <p>/</p>
      <a>Shoes</a>
    </div>
    <div class="lg:flex md:hidden sm:hidden hidden flex-col gap-y-[18px]">
      <a v-for="(item, index) in sideItems" :key="index">{{ item.name }}</a>
    </div>
  </div>
</template>
