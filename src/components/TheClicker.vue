<template>
  <div>
    <h3>TheClicker</h3>
    <button @click="click">Click me too</button>
  </div>
</template>

<script setup lang="ts">
const emit = defineEmits(["updateCounter"]);

const click = () => {
  emit("updateCounter");
}
</script>
