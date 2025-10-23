<script setup>
import { defineProps } from 'vue'
import { homeArt } from '~/data/art-main.js'

const props = defineProps({
  items: {
    type: Array,
    default: () => homeArt
  }
})

</script>
<template>
  <section class="mt-16 py-8">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
        <div
            v-for="item in homeArt"
            :key="item.id"
            class="flex flex-col"
        >
          <!-- Link wrapper for each art item -->
          <NuxtLink :to="item.link" class="w-full h-full overflow-hidden rounded-md">
            <img
                :src="item.image"
                :alt="item.title"
                class="w-full h-full object-cover transform transition-transform duration-300 hover:scale-105"
                loading="lazy"
            />
          </NuxtLink>

          <!-- Always-visible info -->
          <div class="mt-4 space-y-1">
            <h3 class="text-lg font-semibold">{{ item.title }}</h3>

            <p class="text-gray-600">{{ item.size }}</p>
            <p class="text-gray-600">{{ item.medium }}</p>
            <p class="text-gray-800 font-bold">${{ item.price }}</p>
            <NuxtLink :to="item.link">View</NuxtLink>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
