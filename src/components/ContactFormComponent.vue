<template>
  <TitleComponent>Formulaire</TitleComponent>
  <Card>
    <form class="max-w-96 mx-auto mt-5">
      <fieldset>
        <Input type="text" id="name" v-model="name" />
        <Input type="email" id="email" v-model="email" />
        <Input type="text" id="subject" v-model="subject" />
        <Input type="text" id="message" v-model="message" />
      </fieldset>
      <Button class="mt-3" @click.prevent="showInputValue">Envoyer</Button>
    </form>
  </Card>

  <Card v-if="isSend">
    <p>Nom : {{ name }}</p>
    <p>Email : {{ email }}</p>
    <p>Sujet : {{ subject }}</p>
    <p>Message : {{ message }}</p>
  </Card>
</template>

<script setup lang="ts">
import { ref } from "vue";
import Input from "./Input.vue";
import Button from "./Button.vue";
import TitleComponent from "./TitleComponent.vue";
import Card from "./ui/card/Card.vue";

const name = ref("");
const email = ref("");
const subject = ref("");
const message = ref("");
const isSend = ref(false);

const showInputValue = () => {
  isSend.value = !isSend.value;
};
</script>
