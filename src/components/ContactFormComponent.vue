<template>
  <form class="max-w-96 mx-auto mt-5">
    <fieldset>
      <h1>Formulaire de contact</h1>
      <Input type="text" id="name" v-model="name" />
      <Input type="email" id="email" v-model="email" />
      <Input type="text" id="subject" v-model="subject" />
      <Input type="text" id="message" v-model="message" />
    </fieldset>
    <button @click.prevent="showInputValue">Envoyer</button>
  </form>

  <article v-if="isSend">
    <p>Nom : {{ name }}</p>
    <p>Email : {{ email }}</p>
    <p>Sujet : {{ subject }}</p>
    <p>Message : {{ message }}</p>
  </article>
</template>

<script setup lang="ts">
import { ref } from "vue";
import Input from "./Input.vue";

const name = ref("");
const email = ref("");
const subject = ref("");
const message = ref("");
const isSend = ref(false);

const showInputValue = () => {
  isSend.value = !isSend.value;
};
</script>
