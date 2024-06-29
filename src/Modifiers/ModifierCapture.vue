<script setup lang="ts">
const captureFrom = () => {
  alert('capture From');
};

const propagationFrom = () => {
  alert('propagatio From');
};

const captureDiv = () => {
  alert('capture Div');
};

const propagationDiv = () => {
  alert('propagation Div');
};

const captureP = () => {
  alert('capture P');
};

const propagationP = () => {
  alert('propagation P');
};
</script>

<template>
  <seption>
    <h4>modificador capture (addEventListener capture)</h4>
    <p>* por defecto esta opcion de EventListener esta apagada</p>
    <p>
      * por defecto no podemos acceder al proceso de captura de ventos (el
      primer paso antes de la propagacion)
    </p>
    <p>
      pero podemos acceder al proceso de captura de ventos activando el capture
      del eventListener (en este caso lo activamos con el modificador)
    </p>
    <form class="boder" @click.capture="captureFrom" @click="propagationFrom">
      FORM
      <div class="boder" @click.capture="captureDiv" @click="propagationDiv">
        DIV
        <p class="boder" @click.capture="captureP" @click="propagationP">P</p>
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
