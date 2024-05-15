<script setup>
import SectionContainer from "@/components/SectionContainer.vue";

const navLinks = ["Home", "About", "Contact", "Blog", "Careers"];
</script>

<template>
  <header class="bg-white">
    <SectionContainer
      class="flex h-20 justify-between items-center px-6 md:px-12"
    >
      <img src="/logo.svg" alt="logo" />

      <nav
        aria-label="main navigation"
        class="hidden md:flex h-full gap-x-8 items-stretch text-neutral-400"
      >
        <a
          href="/"
          class="flex items-center hover:text-neutral-700 border-b-2 border-b-transparent hover:border-b-green-500"
          v-for="navLink in navLinks"
          :key="navLink"
          >{{ navLink }}</a
        >
      </nav>

      <button
        class="bg-gradient-to-r hidden md:block from-lime-500 font-medium to-cyan-500 text-white px-6 py-2 rounded-full"
      >
        Request Invite
      </button>

      <button class="md:hidden" aria-label="open mobile navigation">
        <img src="/icon-hamburger.svg" aria-hidden="true" alt="" />
      </button>
    </SectionContainer>
  </header>
</template>
