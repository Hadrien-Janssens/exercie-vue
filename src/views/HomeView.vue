<script setup lang="ts">
import TitleComponent from "@/components/TitleComponent.vue";
import Button from "../components/Button.vue";
import ContactFormComponent from "@/components/ContactFormComponent.vue";
import Card from "@/components/ui/card/Card.vue";
</script>

<template>
  <main>
    <TitleComponent level="h3">Voici mes beaux boutons</TitleComponent>
    <Card class="flex gap-3 mb-3 p-2">
      <Button>Primary</Button>
      <Button type="secondary">secondary</Button>
      <Button type="danger">danger</Button>
    </Card>
    <hr />

    <ContactFormComponent />
  </main>
</template>
