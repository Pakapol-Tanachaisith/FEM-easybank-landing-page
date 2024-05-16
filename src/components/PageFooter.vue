<script setup>
import { SOCIAL_LINKS } from "@/constants";
import ContainerVue from "@/components/ContainerVue.vue";
</script>

<template>
  <footer class="bg-[#2d314d]">
    <ContainerVue
      class="flex flex-col items-center gap-8 p-8 lg:p-16 lg:items-start lg:flex-row"
    >
      <div class="text-center">
        <img class="mx-auto" src="/logo-dark.svg" alt="logo" />
        <ul class="flex mt-8 gap-x-4 lg:mt-16 lg:gap-x-8">
          <li v-for="link in SOCIAL_LINKS" :key="link.href">
            <a target="_blank" :href="link.href">
              <img :src="link.icon" :alt="link.alt" />
            </a>
          </li>
        </ul>
      </div>
      <nav
        class="grid gap-4 text-center lg:grid-cols-2 lg:text-start text-neutral-300 lg:ml-32 lg:gap-x-16"
      >
        <a href="#" class="hover:text-neutral-100">About Us</a>
        <a href="#" class="hover:text-neutral-100">Contact</a>
        <a href="#" class="hover:text-neutral-100">Blog</a>
        <a href="#" class="hover:text-neutral-100">Careers</a>
        <a href="#" class="hover:text-neutral-100">Support</a>
        <a href="#" class="hover:text-neutral-100">Privacy Policy</a>
      </nav>
      <div class="ml-auto text-center lg:text-end">
        <button
          class="px-6 py-2 font-medium text-white rounded-full bg-gradient-to-r from-lime-500 to-cyan-500"
        >
          Request Invite
        </button>
        <p class="mt-8 text-sm text-slate-400">
          © Easybank. All Rights Reserved
        </p>

        <div class="mt-4 text-xs opacity-50 text-slate-500">
          Challenge by
          <a
            class="text-slate-400"
            href="https://www.frontendmentor.io?ref=challenge"
            target="_blank"
            >Frontend Mentor</a
          >. Coded by
          <a href="#" class="text-slate-400">Pakapol Tanachaisith</a>.
        </div>
      </div>
    </ContainerVue>
  </footer>
</template>
