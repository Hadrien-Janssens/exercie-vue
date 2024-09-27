<script setup lang="ts">
import TitleComponent from "@/components/TitleComponent.vue";
import Button from "../components/Button.vue";
import ContactFormComponent from "@/components/ContactFormComponent.vue";
</script>

<template>
  <main>
    <TitleComponent level="h3">Mon titre de niveau 3</TitleComponent>
    <Button>Primary</Button>
    <Button type="secondary">secondary</Button>
    <Button type="danger">danger</Button>
    <ContactFormComponent />
  </main>
</template>
