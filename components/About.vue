<script setup>

</script>
<template>
  <section class="py-16 px-6">
    <div class="flex flex-col md:flex-row overflow-hidden w-full p-6 ">
      <div class="about-text md:w-1/3 space-y-6 flex flex-col px-6">
        <h2 class="text-5xl font-bold mb-16">The Spear and the Bear</h2>
        <p class="text-xl">

          The name Gerardo traces back to Germanic roots, meaning “spear” and "brave” or
          “strong”. The name symbolizes courage and strength, an identity steeped in resilience and purpose.
          Garcia is a Spanish surname with origins in the Basque country, where it often means “bear” or "oso"
          This heritage blends both strength and instinct, qualities that lie at the heart of my art
          studio, Lanza y Oso. </p>

        <NuxtImg src="/lanzayoso_logo_small.png" width="100px" class="self-center" />



      </div>
      <div class="about-images flex md:flex-row flex-col justify-center md:p-8 ">
        <NuxtImg src="/profile_pic_2.png" sizes="sm:100vw lg:10vw" class="h-[50vh] md:translate-y-12 shadow-lg">
        </NuxtImg>
        <NuxtImg src="/abrazo_de_agave.png" sizes="sm:100vw lg:10vw"
          class="md:translate-y-64 md:-translate-x-32 z-3 md:h-[50vh] shadow-lg"></NuxtImg>
      </div>
    </div>
  </section>

</template>
