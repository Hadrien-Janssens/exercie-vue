<template>
  <p
    :class="{
      'text-6xl': props.level === 'h1',
      'text-4xl': props.level === 'h2',
      'text-2xl': props.level === 'h3',
      'text-xl': props.level === 'h4',
    }"
  >
    <slot></slot>
  </p>
</template>

<script setup lang="ts">
const props = defineProps({
  level: {
    type: String,
    default: "h3",
  },
});
</script>
