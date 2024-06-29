<script setup lang="ts">
const handleClick = (event: Event, saludo: string) => {
  alert(saludo);
};
</script>

<template>
  <button @click="handleClick($event, 'holaaaa')">argument event op1</button>
  <button @click="(event) => handleClick(event, 'holaaaa 2')">
    argument event op2
  </button>
</template>

<style scoped></style>
