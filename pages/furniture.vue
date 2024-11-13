<script setup>
import furniture from '/data/furniture.js' 
</script>
<template>
  <div class="flex flex-col mt-32">
    <AppBackButton />
    <div class="art-container grid lg:grid-cols-3 gap-2 overflow-y-auto dark:text-white mt-16">
      <NuxtLink :to="mueble.link" v-for="mueble in furniture" :key="mueble.id"
        class="hover:shadow-xl p-4 duration-100 dark:hover:text-red-200">
        <div class="grid place-content-center ">
          <p class="art-title font-bold text-2xl">{{ mueble.title }}</p>
          <NuxtImg :src="mueble.image" sizes="sm:100vw md:100vw" preload :alt="mueble.alt" format="webp"></NuxtImg>
        </div>
      </NuxtLink>
    </div>
  </div>
</template>
