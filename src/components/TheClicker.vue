<template>
  <div>
    <h3>TheClicker</h3>
    <button @click="click">Click me too</button>
  </div>
</template>

<script setup lang="ts">
const props = defineProps({
  count: {
    type: Number,
    required: true,
  }
})

const emit = defineEmits(["update_counter"]);

const click = () => {
  emit("update_counter", props.count + 1);
}
</script>
