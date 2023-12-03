<script setup>
const post = {
  id: 123,
  title: "Top 5 Websites",
  desciption:
    "Lorem ipsum dolor sit amet consectetur adipisicing elit. Esse tempore quo odit inventore vero voluptatem, architecto est cum dolorum quas tenetur amet.",
};

function trucateDesciption(desciption, wordsCount) {
  if (desciption) {
    let words = desciption.split(" ");
    if (words.length > wordsCount) {
      words = words.slice(0, wordsCount);
      return words.join(" ") + "...";
    }
    return desciption;
  }
  return "";
}
</script>

<template>
  <div
    class="bg-gray-600 rounded-lg shadow-lg overflow-hidden flex flex-col md:flex-row mx-auto py-4 max-w-5x1 mt-3"
  >
    <div class="w-full md:w-1/6 P-4">
      <img
        src="/images/laptop.jpg"
        alt="Post Image"
        class="w-full h-auto object-cover"
      />
    </div>
    <div class="w-full md:w-2/3 px-6 py-4">
      <h2 class="text-2xl font-bold md-2 text-white">{{ post.title }}</h2>
      <p class="text-white text-base mb-4">
        {{ trucateDesciption(post.desciption, 10) }}
      </p>
      <NuxtLink
        :to="'/posts/' + post.id"
        class="bg-slate-500 hover:bg-slate-700 text-white font-bold py-2 px-4 rounded"
        >Read More</NuxtLink
      >
    </div>
  </div>
</template>

<style scoped></style>
