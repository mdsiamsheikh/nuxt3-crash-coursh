<script setup></script>

<template>
  <nav class="bg-gray-800">
    <div class="max-w-7xl mx-auto px-2 sm:px-6 lg:px-8">
      <div class="relative flex items-center justify-between h-16">
        <div class="hidden sm:block sm:ml-6">
          <div class="flex space-x-4">
            <NuxtLink
              to="/"
              class="text-white px-3 py-2 rounded-md text-sm font-medium"
              >Home</NuxtLink
            >
            <NuxtLink
              to="/about"
              class="text-gray-300 hover:bg-gray-700 hover:text-white text-white px-3 py-2 rounded-md text-sm font-medium"
              >About</NuxtLink
            >
            <NuxtLink
              to="/contact"
              class="text-gray-300 hover:bg-gray-700 hover:text-white text-white px-3 py-2 rounded-md text-sm font-medium"
              >Contact</NuxtLink
            >
          </div>
        </div>
      </div>
    </div>
  </nav>
</template>

<style scoped></style>
