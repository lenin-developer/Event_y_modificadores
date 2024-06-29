<script setup lang="ts">
const handleClick = (event: Event) => {
  alert('evita que la pagina se recarge despues de un submit');
};
</script>

<template>
  <!-- el modificador prevent -->
  <form @submit.prevent="handleClick">
    <button type="submit">modificador prevent</button>
  </form>
</template>

<style scoped></style>
