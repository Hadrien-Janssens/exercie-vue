<template>
  <form class="max-w-96 mx-auto mt-5">
    <fieldset>
      <h1>Formulaire de contact</h1>
      <Label for="name">
        Nom :
        <input type="text" name="name" id="name" v-model="name" />
      </Label>
      <Label for="email">
        Email :
        <input type="email" name="email" id="email" v-model="email" />
      </Label>
      <Label for="subject">
        Sujet :
        <input type="text" name="subject" id="subject" v-model="subject" />
      </Label>
      <Label for="message">
        Message :
        <input type="text" name="message" id="message" v-model="message" />
      </Label>
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

const name = ref("");
const email = ref("");
const subject = ref("");
const message = ref("");
const isSend = ref(false);

const showInputValue = () => {
  isSend.value = !isSend.value;
};
</script>
