<!--
  author:        xzl_2021 <zilong@ftsafe.com>
  date:          2024-01-31 14:25:12
  component:     login
  Copyright © YourCompanyName All rights reserved
-->
<template>
  <div class="flex justify-center items-center h-screen">
    <form class="w-full max-w-md" @submit.prevent="submitForm">
      <div class="mb-4">
        <label for="name" class="block text-gray-700 text-sm font-bold mb-2">Name:</label>
        <input
          type="text"
          id="name"
          v-model="name"
          class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
          required
        />
      </div>
      <div class="mb-4">
        <label for="age" class="block text-gray-700 text-sm font-bold mb-2">Age:</label>
        <input
          type="number"
          id="age"
          v-model="age"
          class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
        />
      </div>
      <div class="mb-4">
        <label for="profession" class="block text-gray-700 text-sm font-bold mb-2"
          >Profession:</label
        >
        <input
          type="text"
          id="profession"
          v-model="profession"
          class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
          required
        />
      </div>
      <div class="mb-6">
        <label for="gender" class="block text-gray-700 text-sm font-bold mb-2">Gender:</label>
        <div class="relative">
          <select
            id="gender"
            v-model="gender"
            class="block appearance-none w-full border rounded py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
          >
            <option value="male">Male</option>
            <option value="female">Female</option>
            <option value="other">Other</option>
          </select>
          <div
            class="pointer-events-none absolute inset-y-0 right-0 flex items-center px-2 text-gray-700"
          >
            <svg
              class="fill-current h-4 w-4"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 20 20"
            >
              <path d="M10 12a2 2 0 100-4 2 2 0 000 4z" />
            </svg>
          </div>
        </div>
      </div>
      <div class="flex items-center justify-between">
        <button
          type="submit"
          class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded focus:outline-none focus:shadow-outline"
        >
          Submit
        </button>
      </div>
    </form>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const name = ref('')
const age = ref(null)
const profession = ref('')
const gender = ref('male')

function submitForm() {
  // Handle form submission here
  console.log('Form submitted:', name.value, age.value, profession.value, gender.value)
}
</script>

<style>
/* Tailwind CSS classes can be used here */
</style>
