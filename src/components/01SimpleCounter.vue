<template>
  <h2>Contador Simple</h2>
  <p>Contador: {{ counter }}</p>
  <p>{{ counterComputed }}</p>
  <button @click="increment">Incrementar</button>
  <button @click="decrement">Decrementar</button>
</template>
  
<script>
import { ref, computed } from "vue";
export default {
  name: "SimpleCounter",
  setup() {
    const counter = ref(0);

    const counterComputed = computed(() => {
      return `El valor del computed es: ${counter.value}`;
    });

    const increment = () => {
      counter.value++;
    };
    const decrement = () => {
      counter.value--;
    };

    return {
      counter,
      increment,
      decrement,
      counterComputed, // Agregamos el cálculo computado al objeto retornado
    };
  },
};
</script>
  
<style>
</style>
