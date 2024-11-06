<script setup>
import homeArt from "/data/art-main.js"
</script>
<template>
  <div class="py-16">
    <h4 class="text-4xl font-bold">Art for Sale</h4>

    <div class="art-grid-container grid md:grid-cols-3 gap-4 px-6">

      <div class="art-card max-w-[35rem] bg-white hover:shadow-xl flex flex-col p-4" v-for="art in homeArt"
        :key="art.id">

        <NuxtImg :src="art.image" class="self-center max-h-[55vh]"></NuxtImg>
        <p class="art-card-title font-bold text-2xl">{{ art.title }}</p>
        <p class="art-card-price text-lg  font-bold">${{ art.price }}</p>
        <p class="art-card-size  ">{{ art.size }}</p>
        <p class="art-card-medium">{{ art.medium }}</p>


        <NuxtLink to="/" class="font-bold hover:text-red-300 text-xl">Purchase</NuxtLink>
      </div>


    </div>

    <NuxtLink to="/art" class="text-5xl hover:text-red-300 animate-pulse py-4">see more</NuxtLink>
  </div>
</template>
