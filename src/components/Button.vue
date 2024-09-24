<template>
  <button
    class="shadow p-2 px-4 rounded-full"
    :class="{
      'text-blue-200 bg-blue-700': props.type === 'primary',
      'text-gray-200 bg-gray-700': props.type === 'secondary',
      'text-red-200 bg-red-700': props.type === 'danger',
    }"
  >
    <slot></slot>
  </button>
</template>

<script setup lang="ts">
const props = defineProps({
  type: {
    type: String,
    default: "primary",
  },
});
</script>
