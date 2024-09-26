<template>
  <nav class="p-5 flex justify-end">
    <div :class="isOpen ? 'block' : 'hidden'">
      <div
        class="absolute right-0 top-0 flex flex-col j gap-5 md:hidden bg-blue-300 h-screen w-1/2 items-end p-5"
      >
        <i
          @click="isOpen = !isOpen"
          class="ri-close-large-line text-blue-700 text-4xl md:hidden"
          :class="isOpen ? 'block' : 'hidden'"
        ></i>
        <div class="flex flex-col gap-5 h-full">
          <Link @click="isOpen = !isOpen" to="/">Home</Link>
          <Link @click="isOpen = !isOpen" to="/about">About</Link>
        </div>
      </div>
    </div>
    <i
      @click="isOpen = !isOpen"
      class="ri-menu-3-fill text-blue-700 text-4xl md:hidden"
    ></i>

    <div class="hidden md:flex justify-end gap-5">
      <Link to="/">Home</Link>
      <Link to="/about">About</Link>
    </div>
  </nav>
</template>

<script setup lang="ts">
import { ref } from "vue";
import Link from "./Link.vue";
const isOpen = ref(false);
</script>
