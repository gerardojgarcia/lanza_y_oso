<script setup>
import homeArt from "/data/art-main.js"





</script>
<template>
  <div class="mt-10 py-16 ">
    <h1 class="text-4xl font-bold">LanzayOso</h1>

    <div class="art-grid-container grid  px-6 max-h-[70vh] overflow-hidden overflow-y-auto">

      <div class="art-card  bg-white hover:shadow-xl flex flex-col p-4" v-for="art in homeArt" :key="art.id">

        <NuxtImg :src="art.image" class="self-center "></NuxtImg>

        <div class="flex w-full border-2 py-4 justify-evenly">
          <p class="art-card-title font-bold text-2xl">{{ art.title }}</p>
          <p class="art-card-price text-lg  font-bold">${{ art.price }}</p>
          <p class="art-card-size  ">{{ art.size }}</p>
          <p class="art-card-medium">{{ art.medium }}</p>
          <NuxtLink to="/" class="font-bold hover:text-red-300 text-xl">Purchase</NuxtLink>

        </div>



      </div>
    </div>

    <NuxtLink to="/art" class="text-5xl hover:text-red-300 animate-pulse py-4">see more</NuxtLink>
  </div>
</template>
