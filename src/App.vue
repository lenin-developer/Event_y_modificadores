<script setup lang="ts">
import HelloWorld from './components/HelloWorld.vue';
import FooterV from './components/FooterV.vue';
import EventsInterno from './events/EventsInterno.vue';
import EventsExterno from './events/EventsExterno.vue';
import ArgumentEvent from './arguments/ArgumentEvent.vue';
import EventModifiers from './Modifiers/ModifiPrevent.vue';
import ModifiStop from './Modifiers/ModifiStop.vue';
import ModifierSelf from './Modifiers/ModifierSelf.vue';
import ModifierCapture from './Modifiers/ModifierCapture.vue';
import ModifierOnce from './Modifiers/ModifierOnce.vue';
import ModifierEnter from './Modifiers/ModifierEnter.vue';
import ModifierRight from './Modifiers/ModifierRight.vue';

const handleClick = (event: Event) => {
  event.preventDefault();
  alert('click');
};

const atributteHijo = (e: Event, mensaje: string) => {
  event.preventDefault();
  alert(mensaje);
};
</script>

<template>
  <HelloWorld msg="Vite + Vue" />
  <h2>Evento</h2>

  <EventsInterno />
  <EventsExampleB @click="handleClick" />
  <hr />
  <h2>Arguments</h2>
  <ArgumentEvent @click="atributteHijo" />
  <hr />
  <h2>Modificadores de eventos</h2>
  <EventModifiers />
  <ModifierOnce />
  <ModifiStop />
  <ModifierSelf />
  <ModifierCapture />
  <h2>modificadores de teclas</h2>
  <ModifierEnter />
  <h2>modificado de raton</h2>
  <ModifierRight />
  <br />
  <p>
    Nota: los modificadores se puden combinar y el orden es importamte tambien
    (visitar la doc)
  </p>
  <hr />
  <FooterV />
</template>

<style scoped></style>
