<script setup>
const title = ref("Top 5 Websites");
const desciption = ref(
  "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Nihil repellendus odit blanditiis, quis eligendi quas modi exercitationem sequi laudantium nam ullam atque minus ea, soluta minima vero. Cupiditate inventore est sit excepturi laborum non vero? Dolorem doloremque incidunt tempora consequuntur veritatis atque, dicta fugiat."
);
const image = ref("/images/computer.jpg");
</script>

<template>
  <div class="max-w-5xl mx-auto bg-gray-600 shadow-lg overflow-hidden">
    <img :src="image" alt="Post Image" class="w-full h-96 object-cover" />
    <div class="p-6">
      <h1 class="text-white text-3xl font-bold mb-4">{{ title }}</h1>
      <p class="text-gray-200 text-lg mb-4">{{ desciption }}</p>
      <p class="text-gray-200 text-lg mb-4">{{ desciption }}</p>
      <div class="flex items-center mt-10">
        <span class="mr-2 text-white">Share on:</span>
        <NuxtLink to="#" target="_blank" class="mr-2">
          <Icon name="uil:facebook" class="text-white" />
        </NuxtLink>
        <NuxtLink to="#" target="_blank" class="mr-2">
          <Icon name="uil:instagram" class="text-white" />
        </NuxtLink>
      </div>
    </div>
  </div>
</template>

<style scoped></style>
