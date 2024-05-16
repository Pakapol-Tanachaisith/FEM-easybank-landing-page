<script setup>
import { LATEST_ARTICLES } from "@/constants";
import ContainerVue from "@/components/ContainerVue.vue";
import ArticleItem from "@/components/ArticleItem.vue";
</script>

<template>
  <section class="bg-neutral-50">
    <ContainerVue class="px-8 py-16 lg:p-24">
      <h2 class="text-4xl text-center lg:text-left text-neutral-900">
        Latest Articles
      </h2>
      <ul class="grid items-stretch gap-8 mt-12 lg:grid-cols-4 lg:mt-16">
        <li v-for="article in LATEST_ARTICLES" :key="article.img">
          <ArticleItem v-bind="article" />
        </li>
      </ul>
    </ContainerVue>
  </section>
</template>
