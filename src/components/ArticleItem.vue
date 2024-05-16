<script setup>
defineProps({
  author: String,
  title: String,
  img: String,
  content: String,
});
</script>

<template>
  <article class="overflow-hidden bg-white rounded-lg shadow-sm">
    <img
      class="object-cover w-full aspect-video"
      :src="img"
      role="presentation"
      alt=""
    />
    <div class="p-8 lg:p-6">
      <p class="text-xs text-neutral-400">By {{ author }}</p>
      <h3 class="my-4 text-lg font-medium lg:my-2">{{ title }}</h3>
      <p class="text-neutral-400 lg:text-sm">{{ content }}</p>
    </div>
  </article>
</template>
