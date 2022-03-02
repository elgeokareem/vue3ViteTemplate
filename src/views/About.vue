<template>
  <div class="about">
    <h1>This is an about page</h1>
    <p class="parrafo">Text enviroment variable:{{ test }}</p>

    <button @click="incrementCounter">
      {{ counter.count }}
    </button>
  </div>
</template>

<script setup lang="ts">
import { useCounterStore } from "../stores/counter";

const counter = useCounterStore()
const test = import.meta.env.VITE_LOL

function incrementCounter() {
  counter.increment()
}
</script>

<style lang="scss" scoped>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }
}
</style>
