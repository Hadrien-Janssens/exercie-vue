<template>
  <Button
    :class="{
      ' bg-blue-700 hover:bg-blue-800': props.type === 'primary',
      ' bg-gray-700 hover:bg-gray-800': props.type === 'secondary',
      ' bg-red-700 hover:bg-red-800': props.type === 'danger',
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
