<script setup>
import SectionContainer from "@/components/SectionContainer.vue";
import FeatureItem from "@/components/FeatureItem.vue";
import { FEATURES } from "@/constants";
</script>

<template>
  <section class="bg-neutral-100">
    <SectionContainer class="px-8 py-16 lg:p-24">
      <article class="text-center lg:text-left">
        <h2 class="w-3/4 mx-auto text-4xl lg:mx-0 text-neutral-900">
          Why choose Easybank?
        </h2>
        <p class="mt-8 text-neutral-500 lg:w-1/2">
          We leverage Open Banking to turn your bank account into your financial
          hub. Control your finances like never before.
        </p>
      </article>
      <ul class="grid gap-8 mt-12 lg:grid-cols-4 lg:mt-16">
        <li v-for="feature in FEATURES" :key="feature.title">
          <FeatureItem v-bind="feature" />
        </li>
      </ul>
    </SectionContainer>
  </section>
</template>
