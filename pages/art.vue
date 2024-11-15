<script setup>
import { collection } from "./data/art.js";



</script>
<template>
  <div class=" mt-32">
    <AppBackButton />
    <ClientOnly>
      <ShopifyArtCollection />

    </ClientOnly>
  </div>
</template>
