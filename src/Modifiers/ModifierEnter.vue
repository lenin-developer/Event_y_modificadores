<script setup lang="ts">
import { ref } from 'vue';
import type { Ref } from 'vue';

const input: Ref<string> = ref('');

const handleClick = (event: Event) => {
  alert(input.value);
  input.value = '';
};
</script>

<template>
  <h4>modificador enter</h4>
  <p>exiten muchos modificadores de este tipo (ver doc)</p>
  <span>escriba y precione enter</span>
  <input type="text" v-model="input" @keyup.enter="handleClick" />
</template>

<style scoped></style>
