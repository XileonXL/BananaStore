<template>
  <div class="container mx-auto p-8 max-w-4xl">
    <!-- Header Section with Tailwind utilities -->
    <div class="mb-8">
      <h1 class="text-4xl font-bold text-center mb-4 bg-gradient-to-r from-purple-600 to-blue-600 bg-clip-text text-transparent">
        Vue 3 + Vite + Tailwind + DaisyUI
      </h1>
      <p class="text-center text-lg text-gray-600 dark:text-gray-300">
        A test component showcasing Tailwind CSS utilities and DaisyUI components
      </p>
    </div>

    <!-- DaisyUI Card Components -->
    <div class="grid grid-cols-1 md:grid-cols-2 gap-6 mb-8">
      <!-- Card 1 -->
      <div class="card bg-base-100 shadow-xl">
        <div class="card-body">
          <h2 class="card-title text-primary">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z" />
            </svg>
            DaisyUI Card #1
          </h2>
          <p class="text-base-content">This is a beautiful card component from DaisyUI with Tailwind styling.</p>
          <div class="card-actions justify-end">
            <button class="btn btn-primary" @click="incrementCounter">
              Clicked {{ counter1 }} times
            </button>
          </div>
        </div>
      </div>

      <!-- Card 2 -->
      <div class="card bg-gradient-to-br from-secondary to-accent shadow-xl text-white">
        <div class="card-body">
          <h2 class="card-title">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 3v4M3 5h4M6 17v4m-2-2h4m5-16l2.286 6.857L21 12l-5.714 2.143L13 21l-2.286-6.857L5 12l5.714-2.143L13 3z" />
            </svg>
            DaisyUI Card #2
          </h2>
          <p>This card features a gradient background using Tailwind utilities.</p>
          <div class="card-actions justify-end">
            <button class="btn btn-ghost bg-white/20 hover:bg-white/30" @click="incrementCounter2">
              Clicked {{ counter2 }} times
            </button>
          </div>
        </div>
      </div>
    </div>

    <!-- DaisyUI Button Showcase -->
    <div class="mb-8">
      <h3 class="text-2xl font-semibold mb-4 text-center">DaisyUI Button Variants</h3>
      <div class="flex flex-wrap gap-3 justify-center">
        <button class="btn">Default</button>
        <button class="btn btn-primary">Primary</button>
        <button class="btn btn-secondary">Secondary</button>
        <button class="btn btn-accent">Accent</button>
        <button class="btn btn-success">Success</button>
        <button class="btn btn-warning">Warning</button>
        <button class="btn btn-error">Error</button>
        <button class="btn btn-outline btn-info">Outline Info</button>
      </div>
    </div>

    <!-- Additional DaisyUI Components -->
    <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
      <!-- Alert Component -->
      <div class="alert alert-info shadow-lg">
        <div>
          <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" class="stroke-current flex-shrink-0 w-6 h-6">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 16h-1v-4h-1m1-4h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z"></path>
          </svg>
          <span>This is a DaisyUI alert component!</span>
        </div>
      </div>

      <!-- Badge Component -->
      <div class="flex items-center justify-center gap-2 p-4 bg-base-200 rounded-lg">
        <span class="badge badge-primary">Badge</span>
        <span class="badge badge-secondary">Badge</span>
        <span class="badge badge-accent">Badge</span>
        <span class="badge badge-ghost">Badge</span>
      </div>
    </div>

    <!-- Tailwind Utilities Showcase -->
    <div class="mt-8 p-6 bg-base-200 rounded-lg">
      <h3 class="text-2xl font-semibold mb-4 text-center">Tailwind Utility Classes in Action</h3>
      <div class="flex flex-col sm:flex-row gap-4 justify-center items-center">
        <div class="w-24 h-24 bg-blue-500 rounded-full shadow-lg transform hover:scale-110 transition-transform duration-300"></div>
        <div class="w-24 h-24 bg-green-500 rounded-lg shadow-lg transform hover:rotate-45 transition-transform duration-300"></div>
        <div class="w-24 h-24 bg-red-500 rounded shadow-lg transform hover:skew-y-12 transition-transform duration-300"></div>
      </div>
      <p class="text-center mt-4 text-sm text-gray-500">Hover over the shapes to see Tailwind transitions!</p>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const counter1 = ref(0)
const counter2 = ref(0)

const incrementCounter = () => {
  counter1.value++
}

const incrementCounter2 = () => {
  counter2.value++
}
</script>
