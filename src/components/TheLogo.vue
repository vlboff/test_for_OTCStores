<template>
  <div class="logo">
    <img :src="props.src" alt="">
  </div>
</template>

<script setup lang="ts">
const props = defineProps({
  src: {
    type: String,
    required: true
  }
})
</script>

<style scoped>
.logo {
  padding: 1rem;
}
.logo img {
  max-width: 300px;
  width: 100%;
}
</style>
