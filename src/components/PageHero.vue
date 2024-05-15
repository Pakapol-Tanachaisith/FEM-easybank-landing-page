<script setup>
import SectionContainer from "@/components/SectionContainer.vue";
</script>

<template>
  <section class="bg-neutral-50">
    <SectionContainer class="relative overflow-hidden">
      <img class="w-full md:hidden" src="/bg-intro-mobile.svg" alt="" />
      <img
        class="absolute right-[-40%] top-[-50%] hidden w-full md:block"
        src="/bg-intro-desktop.svg"
        alt=""
      />
      <img
        class="absolute top-[-15%] md:top-[-15%] md:right-[-8%]"
        src="/image-mockups.png"
        alt=""
      />
      <article
        class="flex-shrink-0 md:w-1/2 md:h-[800px] text-center md:text-start p-8 md:pl-16 md:py-24"
      >
        <h1 class="text-5xl font-medium md:w-3/4">
          Next generation digital banking
        </h1>
        <p class="my-8 text-neutral-400 md:w-3/4 md:my-10">
          Take your financial life online. Your Easybank account will be a
          one-stop-shop for spending, saving, budgeting, investing, and much
          more.
        </p>
        <button
          class="px-6 py-2 font-medium text-white rounded-full bg-gradient-to-r md:block from-lime-500 to-cyan-500"
        >
          Request Invite
        </button>
      </article>
    </SectionContainer>
  </section>
</template>
