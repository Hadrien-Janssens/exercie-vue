<script setup lang="ts">
import "remixicon/fonts/remixicon.css";
import { RouterView } from "vue-router";
import NavigationBar from "./components/NavigationBar.vue";
</script>

<template>
  <header>
    <NavigationBar />
    <div class="wrapper"></div>
  </header>
  <div class="mx-5">
    <RouterView />
  </div>
</template>
