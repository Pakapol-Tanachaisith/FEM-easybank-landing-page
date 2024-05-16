<script setup>
import SectionContainer from "@/components/SectionContainer.vue";
import FeatureItem from "@/components/FeatureItem.vue";

const features = [
  {
    title: `Online Banking`,
    desc: `Our modern web and mobile applications allow you to keep track of your finances 
  wherever you are in the world.`,
    icon: `/icon-online.svg`,
  },
  {
    title: `Simple Budgeting`,
    desc: `See exactly where your money goes each month. Receive notifications when you’re 
  close to hitting your limits.`,
    icon: `/icon-budgeting.svg`,
  },
  {
    title: `Fast Onboarding`,
    desc: `We don’t do branches. Open your account in minutes online and start taking control 
  of your finances right away.`,
    icon: `/icon-onboarding.svg`,
  },
  {
    title: `Open API`,
    desc: `Manage your savings, investments, pension, and much more from one account. Tracking 
  your money has never been easier.`,
    icon: `/icon-api.svg`,
  },
];
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
        <FeatureItem
          v-for="feature in features"
          v-bind="feature"
          :key="feature.title"
        />
      </ul>
    </SectionContainer>
  </section>
</template>
