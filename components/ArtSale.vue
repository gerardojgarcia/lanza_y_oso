<script setup>
import homeArt from "/data/art-main.js"





</script>
<template>
  <div class="mt-10 md:mt-0 w-full">
    <h1 class="text-4xl font-bold">LanzayOso</h1>

    <div class="art-grid-container place-items-center grid grid-cols-1 md:grid-cols-1 px-6 h-[95vh] gap-4 overflow-y-auto">

      <div class="art-card group bg-white hover:shadow-xl flex flex-col p-4" v-for="art in homeArt"
        :key="art.id">

        <NuxtImg :src="art.image" class=" w-full h-auto block "></NuxtImg>

        <div class="opacity-0  group-hover:opacity-100 flex duration-300 w-full border-2 py-4 justify-evenly">
          <p class="art-card-title font-bold text-2xl">{{ art.title }}</p>
          <p class="art-card-price text-lg  font-bold">${{ art.price }}</p>
          <p class="art-card-size  ">{{ art.size }}</p>
          <p class="art-card-medium">{{ art.medium }}</p>
          <NuxtLink to="/" class="font-bold hover:text-red-300 text-xl">Purchase</NuxtLink>

        </div>



      </div>
    </div>


  </div>
</template>
