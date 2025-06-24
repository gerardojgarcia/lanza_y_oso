<script setup lang="ts">
import { ref } from 'vue'
import homeArt from '~/data/art-main.js'

const name = ref('')
const email = ref('')
const selectedArt = ref('')
const message = ref('')

function submitForm() {
  // TODO: replace with real submission logic
  console.log({
    name: name.value,
    email: email.value,
    selectedArt: selectedArt.value,
    message: message.value
  })
  // Reset fields
  name.value = ''
  email.value = ''
  selectedArt.value = ''
  message.value = ''
}
</script>

<template>
  <section class="py-16">
    <div class="max-w-xl mx-auto text-center px-4">
      <!-- Decorator Label -->
      <div class="inline-flex items-center border border-gray-300 rounded-lg px-4 py-2 mb-4 space-x-2">
        <!-- Envelope Icon -->
        <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5 text-gray-700" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8m0 0v8a2 2 0 01-2 2H5a2 2 0 01-2-2V8m18 0L12 13 3 8" />
        </svg>
        <span class="text-gray-700 font-medium">Contact</span>
      </div>

      <!-- Heading -->
      <h2 class="text-4xl font-light mb-2">Get in Touch</h2>
      <p class="text-gray-600 mb-8">Fill out the form below, and we'll respond promptly.</p>

      <!-- Form -->
      <form @submit.prevent="submitForm" class="space-y-4 text-left">
        <input
            v-model="name"
            type="text"
            placeholder="Name"
            class="w-full bg-gray-100 rounded-lg px-4 py-3 focus:outline-none focus:ring-2 focus:ring-gray-300"
            required
        />
        <input
            v-model="email"
            type="email"
            placeholder="yourMail@mail.com"
            class="w-full bg-gray-100 rounded-lg px-4 py-3 focus:outline-none focus:ring-2 focus:ring-gray-300"
            required
        />

        <!-- Dropdown list pulled from homeArt data -->
        <select
            v-model="selectedArt"
            class="w-full bg-gray-100 rounded-lg px-4 py-3 focus:outline-none focus:ring-2 focus:ring-gray-300"
            required
        >
          <option value="" disabled>Select an art piece</option>
          <option
              v-for="(item, index) in homeArt"
              :key="index"
              :value="item.title"
          >
            {{ item.title }}
          </option>
        </select>

        <textarea
            v-model="message"
            rows="6"
            placeholder="Your message..."
            class="w-full bg-gray-100 rounded-lg px-4 py-3 focus:outline-none focus:ring-2 focus:ring-gray-300 resize-none"
            required
        />
        <button
            type="submit"
            class="w-full bg-black text-white py-4 rounded-full font-medium hover:bg-gray-900 transition"
        >
          Submit
        </button>
      </form>
    </div>
  </section>
</template>

<style scoped>

</style>