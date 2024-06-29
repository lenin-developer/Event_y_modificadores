<script setup lang="ts">
const handleClick = (event: Event) => {
  alert('solo se ejecuta una vez');
};
</script>

<template>
  <button @click.once="handleClick">modificador once</button>
</template>

<style scoped></style>
