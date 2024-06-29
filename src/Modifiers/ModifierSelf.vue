<script setup lang="ts">
const clickFrom = () => {
  alert('From');
};

const clickDiv = () => {
  alert('Div');
};

const clickP = () => {
  alert('P');
};
</script>

<template>
  <seption>
    <h4>modificador selt</h4>
    <span
      >solo activa el evento si el event.target es el mismo elemento en si, es
      decir, que no se active el evento desde una propagacion de un elemento
      hijo)</span
    >
    <form class="boder" @click="clickFrom">
      FORM
      <div class="boder" @click.self="clickDiv">
        DIV (self)
        <p class="boder" @click="clickP">P</p>
      </div>
    </form>
  </seption>
</template>

<style scoped>
.boder {
  margin: 10px;
  border: 1px solid blue;
}
</style>
