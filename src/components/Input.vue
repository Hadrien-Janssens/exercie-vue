<template>
  <Label :for="id">
    {{ id && id.charAt(0).toUpperCase() + id.slice(1) }} :
    <Input :type="type" :name="id" :id="id" v-model="model" />
  </Label>
</template>

<script setup lang="ts">
import Input from "./ui/input/Input.vue";

defineProps({
  type: String,
  id: String,
  modelValue: String,
});

const model = defineModel();
</script>
