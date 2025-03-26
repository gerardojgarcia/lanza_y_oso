<script setup>
import photographs from './data/photography.js'
</script>
<template>

  <div class="flex flex-col mt-8">
    <AppBackButton />
    <div class="art-container grid lg:grid-cols-1 gap-2 overflow-y-auto max-h-[85vh] dark:text-white mt-16">
      <NuxtLink :to="pic.link" v-for="pic in photographs" :key="pic.id"
        class="hover:shadow-xl p-4 duration-100 dark:hover:text-red-200">
        <div class="grid place-content-center ">
          <p class="art-title font-bold text-2xl">{{ pic.title }}</p>
          <NuxtImg :src="pic.img" sizes="sm:100vw md:100vw" preload :alt="pic.alt" format="webp"></NuxtImg>
        </div>
      </NuxtLink>
    </div>
  </div>


</template>
