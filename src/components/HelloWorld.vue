<template>
  <div>
    <p>Computed Property: {{ fullName }}</p>
    <p>Reactive Property: {{ firstName }}</p>
  </div>
</template>

<script lang="ts" setup>
import { ref, computed } from "vue";

// Define reactive properties
const firstName = ref("John");
const lastName = ref("Doe");

// Define a computed property
const fullName = computed(() => {
  return `${firstName.value} ${lastName.value}`;
});
</script>
