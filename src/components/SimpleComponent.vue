<script setup lang="ts">
const model = defineModel<string | number>({ required: true });

const typeofModel = typeof model.value === "number" ? "number" : "text";
</script>

<template>
  <input v-model="model" :type="typeofModel" />
</template>
