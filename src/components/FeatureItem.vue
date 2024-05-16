<script setup>
defineProps({
  title: String,
  desc: String,
  icon: String,
});
</script>

<template>
  <article class="text-center lg:text-left">
    <img class="mx-auto lg:ml-0" :src="icon" aria-hidden="true" alt="" />
    <h3 class="my-6 text-xl text-neutral-700">{{ title }}</h3>
    <p class="text-neutral-500">{{ desc }}</p>
  </article>
</template>
