<script setup></script>
<template>
  <div>
    <div class="grid md:grid-cols-2 mt-32 pb-12 px-12">
      <div class="text-black flex flex-col items-center justify-center  space-y-4 ">
        <h1 class="text-5xl hidden md:block self-start">Lanza y Oso</h1>
        <p class="px-2 text-xl md:px-0 md:w-3/4">
          a multidisciplinary art studio in East Los Angeles founded by Gerardo García.
        </p>

      </div>
      <div>
        <NuxtImg src="/art/timewasters.webp" alt="Img of Gerardo Garcia" height="800px" width="600px"
          class="hidden md:block grayscale opacity-75%" />
        <NuxtImg src="/lanzayoso.png" class="md:hidden" />
      </div>
    </div>
  </div>
</template>
