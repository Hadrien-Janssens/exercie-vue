<template>
  <Button
    :class="{
      'text-blue-200 bg-blue-700': props.type === 'primary',
      'text-gray-200 bg-gray-700': props.type === 'secondary',
      'text-red-200 bg-red-700': props.type === 'danger',
    }"
  >
    <slot></slot>
  </Button>
</template>

<script setup lang="ts">
import { Button } from "./ui/button";

const props = defineProps({
  type: {
    type: String,
    default: "primary",
  },
});
</script>
