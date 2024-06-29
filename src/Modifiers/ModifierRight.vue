<script setup lang="ts">
const handleClick = (event: Event) => {
  alert(' se preciono click derecho');
};
</script>

<template>
  <h4>modificador ringht</h4>
  <p>exiten mas de este tipo (ver doc)</p>
  <div @click.right="handleClick">
    <p>da click derecho dentro del cuadro</p>
  </div>
</template>

<style scoped>
div {
  width: 100%;
  height: 100px;
  background: red;
  color: white;
}
</style>
