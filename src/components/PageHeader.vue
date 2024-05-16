<script setup>
import ContainerVue from "@/components/ContainerVue.vue";
import { useMobileNavigation } from "@/stores/mobileNavigation";

const mobileNav = useMobileNavigation();

const navLinks = ["Home", "About", "Contact", "Blog", "Careers"];
</script>

<template>
  <header class="bg-white">
    <ContainerVue class="flex items-center justify-between h-20 px-8 md:px-16">
      <img src="/logo.svg" alt="logo" />

      <nav
        aria-label="main navigation"
        class="items-stretch hidden h-full md:flex gap-x-8 text-neutral-400"
      >
        <a
          href="/"
          class="flex items-center border-b-2 hover:text-neutral-700 border-b-transparent hover:border-b-green-500"
          v-for="navLink in navLinks"
          :key="navLink"
          >{{ navLink }}</a
        >
      </nav>

      <button
        class="hidden px-6 py-2 font-medium text-white rounded-full bg-gradient-to-r md:block from-lime-500 to-cyan-500"
      >
        Request Invite
      </button>

      <button
        v-if="mobileNav.isOpen"
        @click="mobileNav.onClose"
        class="md:hidden"
        aria-label="close mobile navigation"
      >
        <img src="/icon-close.svg" aria-hidden="true" alt="" />
      </button>
      <button
        v-else
        @click="mobileNav.onOpen"
        class="md:hidden"
        aria-label="open mobile navigation"
      >
        <img src="/icon-hamburger.svg" aria-hidden="true" alt="" />
      </button>
    </ContainerVue>
  </header>
</template>
