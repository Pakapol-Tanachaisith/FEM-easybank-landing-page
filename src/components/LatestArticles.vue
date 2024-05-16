<script setup>
import { LATEST_ARTICLES } from "@/constants";
import SectionContainer from "@/components/SectionContainer.vue";
import ArticleItem from "@/components/ArticleItem.vue";
</script>

<template>
  <section class="bg-neutral-50">
    <SectionContainer class="px-8 py-16 lg:p-24">
      <h2 class="text-4xl text-center lg:text-left text-neutral-900">
        Latest Articles
      </h2>
      <ul class="grid items-stretch gap-8 mt-12 lg:grid-cols-4 lg:mt-16">
        <li v-for="article in LATEST_ARTICLES" :key="article.img">
          <ArticleItem v-bind="article" />
        </li>
      </ul>
    </SectionContainer>
  </section>
</template>
