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
    <h4>modificador stop (stop propagation)</h4>
    <form class="boder" @click="clickFrom">
      FORM
      <div class="boder" @click.stop="clickDiv">
        DIV (stop)
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
