<template>
  <RouterLink :to="to" class="text-xl"><slot></slot></RouterLink>
</template>

<script setup lang="ts">
const props = defineProps({
  to: {
    type: String,
  },
});
</script>
