<template>
  <RouterLink :to="to" class="text-blue-700"><slot></slot></RouterLink>
</template>

<script setup lang="ts">
const props = defineProps({
  to: {
    type: String,
  },
});
</script>
