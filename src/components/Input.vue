<template>
  <Label :for="id">
    {{ id && id.charAt(0).toUpperCase() + id.slice(1) }} :
    <input :type="type" :name="id" :id="id" v-model="model" />
  </Label>
</template>

<script setup lang="ts">
defineProps({
  type: String,
  id: String,
  modelValue: String,
});

const model = defineModel();
</script>
