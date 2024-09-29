<script setup lang="ts">
import TitleComponent from "@/components/TitleComponent.vue";
import Button from "../components/Button.vue";
import ContactFormComponent from "@/components/ContactFormComponent.vue";
import Card from "@/components/ui/card/Card.vue";
</script>

<template>
  <Card class="my-10">
    <TitleComponent level="h1">Les composents titres</TitleComponent>
    <TitleComponent level="h2">Les composents titres</TitleComponent>
    <TitleComponent level="h3">Les composents titres</TitleComponent>
    <TitleComponent level="h4">Les composents titres</TitleComponent>
  </Card>
  <main>
    <TitleComponent level="h3" class="mb-2"
      >Voici mes beaux boutons</TitleComponent
    >
    <Card class="flex gap-3 mb-3 p-2">
      <Button>base</Button>
      <Button type="primary">Primary</Button>
      <Button type="secondary">secondary</Button>
      <Button type="danger">Supprimer</Button>
    </Card>
  </main>
</template>
