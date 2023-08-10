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
