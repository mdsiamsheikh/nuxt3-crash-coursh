<script setup>
const { data, error, pending } = useLazyFetch(
  "https://dummyjson.com/posts?limit=10"
);
console.log(data);
</script>

<template>
  <div>
    <div v-for="{ id, title, body } in data.posts" :key="id">
      <PostCard :id="id" :title="title" :body="body" />
    </div>
  </div>
</template>

<style scoped></style>
