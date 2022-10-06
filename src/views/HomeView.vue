<script setup lang="ts">
import HomeSidemenu from "../components/HomeSidemenu.vue";
import HomeShoesMain from "../components/HomeShoesMain.vue";
import ky from "ky";

ky.get("https://fakestoreapi.com/products")
  .json()
  .then((resp) => {
    console.log(resp);
  });
</script>

<template>
  <main
    class="flex flex-col sm:flex-col md:flex-col lg:flex-row gap-x-[110px] px-[16px] py-6 md:px-[32px] md:py-[78px]"
  >
    <HomeSidemenu />
    <HomeShoesMain />
  </main>
</template>
