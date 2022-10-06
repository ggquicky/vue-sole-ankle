<script setup lang="ts">
import IconShopping from "./icons/IconShopping.vue";
import IconSearch from "./icons/IconSearch.vue";
import IconMenu from "./icons/IconMenu.vue";
const navItems = [
  { name: "Sale", url: "/" },
  { name: "New Releases", url: "/" },
  { name: "Men", url: "/" },
  { name: "Women", url: "/" },
  { name: "Kids", url: "/" },
  { name: "Collection", url: "/" },
];
</script>

<template>
  <div
    class="flex flex-row gap-12 h-20 items-center border-b-2 justify-between lg:justify-start px-[32px] py-[22px]"
  >
    <h1 class="text-3xl lg:w-72">Sole&Ankle</h1>
    <nav class="hidden lg:block" v-for="(item, index) in navItems" :key="index">
      <RouterLink class="text-lg" :to="item.url">{{ item.name }}</RouterLink>
    </nav>
    <nav class="flex gap-5 md:gap-6 lg:hidden">
      <IconShopping />
      <IconSearch />
      <IconMenu />
    </nav>
  </div>
</template>
