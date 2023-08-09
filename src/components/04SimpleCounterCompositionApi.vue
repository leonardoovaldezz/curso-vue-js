<template>
  <h2>Simple Counter Composition API</h2>
  <p>{{ counter }}</p>
  <button @click="increment">Incrementar</button>
  <button @click="decrement">Decrementar</button>
</template>

<script>
import useCounter from "@/composables/useCounter";
export default {
  name: "SimpleCounterCompositionApi",
  setup() {
    const { counter, increment, decrement } = useCounter();
    return { counter, increment, decrement };
  },
};
</script>

<style>
</style>