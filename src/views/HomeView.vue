<script setup lang="ts">
import TitleComponent from "@/components/TitleComponent.vue";
import Button from "../components/Button.vue";
</script>

<template>
  <main>
    <TitleComponent level="h1">Mon titre de niveau 1</TitleComponent>
    <TitleComponent level="h2">Mon titre de niveau 2</TitleComponent>
    <TitleComponent level="h3">Mon titre de niveau 1</TitleComponent>
    <TitleComponent level="h4">Mon titre de niveau 1</TitleComponent>
    <Button>Primary</Button>
    <Button type="secondary">secondary</Button>
    <Button type="danger">danger</Button>
  </main>
</template>
