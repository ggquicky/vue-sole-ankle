<script setup lang="ts">
import image1 from "../assets/image1.png";
import image2 from "../assets/image2.png";
import image3 from "../assets/image3.png";
import image4 from "../assets/image4.png";
import image5 from "../assets/image5.png";
import image6 from "../assets/image6.png";

const data = [
  {
    name: "NikeCourt Tech Challenge 20",
    colors: "2",
    price: "$165",
    discount: "",
    tag: "Just Release!",
    img: image1,
  },
  {
    name: "Nike Metcon 5 AMP",
    colors: "1",
    price: "$165",
    discount: "$145",
    tag: "sale",
    img: image2,
  },
  {
    name: "Nike Phantom Vision",
    colors: "4",
    price: "$165",
    discount: "",
    tag: "Just Release!",
    img: image3,
  },
  {
    name: "Nike Air Zoom Pegasus 36 Trail",
    colors: "2",
    price: "$165",
    discount: "",
    tag: "",
    img: image4,
  },
  {
    name: "Nike Joyride Dual Run",
    colors: "2",
    price: "$170",
    discount: "$100",
    tag: "sale",
    img: image5,
  },
  {
    name: "Nike Tiempo Legend 8 Academy TF",
    colors: "2",
    price: "$165",
    discount: "$80",
    tag: "sale",
    img: image6,
  },
];
</script>

<template>
  <div class="flex flex-col gap-y-[40px]">
    <p class="text-[24px]">Running</p>
    <div
      class="flex gap-[30px] flex-wrap justify-center md:justify-start lg:justify-start"
    >
      <div class="relative" v-for="(shoes, index) in data" :key="index">
        <img
          class="lg:w-[320px] md:w-[336px] w-[342px]"
          :src="shoes.img"
          alt=""
        />
        <p
          v-if="shoes.tag === 'sale'"
          class="absolute top-3 right-1 text-white bg-[#C5295D] rounded-sm p-2"
        >
          {{ shoes.tag }}
        </p>
        <p
          v-else-if="shoes.tag === 'Just Release!'"
          class="text-white bg-[#6868D9] rounded-sm p-2 absolute top-3 right-1"
        >
          {{ shoes.tag }}
        </p>
        <div>
          <div class="flex justify-between">
            <p>{{ shoes.name }}</p>
            <p>{{ shoes.price }}</p>
          </div>
          <div class="flex justify-between">
            <p>{{ shoes.colors }} Colors</p>
            <p class="text-[#C5295D]">{{ shoes.discount }}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
