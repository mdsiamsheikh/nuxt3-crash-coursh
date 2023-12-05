<script setup>
definePageMeta({
  layout: "custom",
});

const route = useRoute();

const {
  data: post,
  error,
  pending,
} = useLazyFetch(`https://dummyjson.com/posts/${route.params.id}`);

console.log(post);
</script>

<template>
  <div class="bg-gray-900">
    <div v-if="error" class="text-2xl text-white">
      Am error occured...{{ error }}
    </div>
    <div v-else-if="post">
      <PostDetail :id="post.id" :title="post.title" :body="post.body" />
    </div>
    <div v-else class="text-2xl text-white">Loading...</div>
  </div>
</template>

<style scoped></style>
