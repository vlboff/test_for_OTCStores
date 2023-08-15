<template>
  <div>
    <h3>TheCounter</h3>
    <slot name="default" :count="count">
      <p>Count: {{ count }}</p>
    </slot>
    <button @click="increment">Click me</button>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';
const emit = defineEmits(["updateCounter"]);
const count = ref(0);

const increment = () => {
  count.value++;
  emit("updateCounter");
}

const simpleIncrement = () => {
  count.value++;
}

defineExpose({
  simpleIncrement,
})
</script>
