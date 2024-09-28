<template>
  <div class="about">
    <TitleComponent level="h2"> Voici mon bouton</TitleComponent>
    <Button>shadcn Btn</Button>
  </div>
</template>

<script setup>
import { Button } from "@/components/ui/button";
import TitleComponent from "@/components/TitleComponent.vue";
</script>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
