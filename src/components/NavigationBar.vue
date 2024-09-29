<template>
  <nav class="p-5 flex justify-between">
    <DarkMode />
    <!-- hamburger menu -->
    <Transition>
      <div
        v-if="isOpen"
        class="absolute right-0 top-0 flex flex-col j gap-5 md:hidden bg-gray-300 h-screen w-1/2 items-end p-5 bg-opacity-10 backdrop-blur-md"
      >
        <i
          @click="isOpen = !isOpen"
          class="ri-close-large-line text-4xl md:hidden"
        ></i>
        <div class="flex flex-col gap-5 h-full">
          <Link @click="isOpen = !isOpen" to="/">Home</Link>
          <Link @click="isOpen = !isOpen" to="/about">About</Link>
          <Link @click="isOpen = !isOpen" to="/contact">Contact</Link>
        </div>
      </div>
    </Transition>
    <i @click="isOpen = !isOpen" class="ri-menu-3-fill text-4xl md:hidden"></i>

    <div class="hidden md:flex justify-end gap-5">
      <Link to="/">Home</Link>
      <Link to="/about">About</Link>
      <Link to="/contact">Contact</Link>
    </div>
  </nav>
</template>

<script setup lang="ts">
import { ref } from "vue";
import Link from "./Link.vue";
import DarkMode from "./DarkMode.vue";

const isOpen = ref(false);
</script>

<style scoped>
.v-enter-active,
.v-leave-active {
  transition: 0.3s ease;
}

.v-enter-from,
.v-leave-to {
  transform: translateX(100%);
}
</style>
