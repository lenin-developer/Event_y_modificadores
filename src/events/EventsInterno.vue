<script setup lang="ts">
const handleClick = (event: Event) => {
  event.preventDefault();
  alert('click');
};
</script>

<template>
  <button type="submit" @click="handleClick">evento interno</button>
</template>

<style scoped></style>
