<script setup></script>
<template>
  <div>
    <div class="grid md:grid-cols-2 mt-32 pb-12 px-12">
      <div class="text-black flex flex-col items-center justify-center  space-y-4 ">
        <h1 class="text-5xl hidden md:block self-start">Lanza y Oso</h1>
  <NuxtLink to="/art" class="text-xl hover:text-blue-500">More</NuxtLink>

      </div>
      <div>
        <NuxtImg src="/21stcenturyfrijole.webp" alt="Img of Gerardo Garcia" height="800px" width="600px"
          class="hidden md:block  opacity-75%" />
        <NuxtImg src="/lanzayoso.webp" class="md:hidden" />
      </div>
    </div>
  </div>
</template>
