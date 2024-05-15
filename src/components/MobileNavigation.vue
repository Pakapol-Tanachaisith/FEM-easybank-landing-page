<script setup>
import { useMobileNavigation } from "@/stores/mobileNavigation";
import { onMounted, onUnmounted } from "vue";

const mobileNav = useMobileNavigation();

const navLinks = ["Home", "About", "Contact", "Blog", "Careers"];

const onEscapeDown = (e) => {
  if (e.key === "Escape") {
    mobileNav.onClose();
  }
};

onMounted(() => {
  document.addEventListener("keydown", onEscapeDown);
});
onUnmounted(() => {
  document.removeEventListener("keydown", onEscapeDown);
});
</script>

<template>
  <Transition>
    <div v-if="mobileNav.isOpen" class="fixed inset-0 top-20 md:hidden">
      <div
        @click="mobileNav.onClose"
        class="absolute inset-0 bg-black/75 -z-10"
      ></div>
      <nav
        class="bg-white w-[90%] mx-auto mt-6 px-6 py-8 rounded-md flex flex-col items-center gap-y-6"
      >
        <a
          href="/"
          v-for="navLink in navLinks"
          :key="navLink"
          @click.prevent="mobileNav.onClose"
          class="text-neutral-800"
          >{{ navLink }}</a
        >
      </nav>
    </div>
  </Transition>
</template>

<style scoped>
.v-enter-active,
.v-leave-active {
  transition: opacity 0.5s ease;
}

.v-enter-from,
.v-leave-to {
  opacity: 0;
}
</style>
