<template>
  <h2>Watch Counter</h2>
  <h3>{{ counter }}</h3>
  <h3>{{ counter2 }}</h3>
  <h3>{{ message }}</h3>
  <button @click="increment">Incrementar</button>
  <button @click="decrement">Decrementar</button>
</template>
  
  <script>
import { ref, watch } from "vue";
export default {
  name: "WatchCounter",
  setup() {
    const counter = ref(0);
    const counter2 = ref(0);
    const message = ref("");

    watch([counter, counter2], () => {
      if (counter.value === 5) {
        message.value = "Counter es 5";
        counter2.value = 10
      } else {
        message.value = "";
      }
      if(counter2.value === 10){
        console.log("Counter 2 ha cambiado")
      }
    });

    const increment = () => {
      counter.value++;
    };
    const decrement = () => {
      counter.value--;
    };
    return {
      counter,
      counter2,
      message,
      increment,
      decrement,
    };
  },
};
</script>
  
  <style>
</style>
  