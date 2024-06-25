<script setup>
import { ref } from "vue";

defineProps({
  msg: String,
});

const count = ref(0);
</script>

<template>
  <h1>Hello</h1>
  <div>
    <p>dasfasf</p>
  </div>
</template>

<style scoped>
div {
  @apply text-red-300;
  p {
    @apply p-2;
  }
}
</style>
