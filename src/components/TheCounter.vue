<template>
  <div>
    <h3>TheCounter</h3>
    <slot name="default">
      <p>Count: {{ count }}</p>
    </slot>
    <button @click="click">Click me</button>
  </div>
</template>

<script setup lang="ts">
import {ref} from "vue";

const count = ref(0)
const click = () => {
  count.value++
}
</script>
