<template>
  <h2>Hola Mundo VUE</h2>
  <p>{{ message }}</p>
  <label for="message">Mensaje</label><br />
  <input type="text" id="message" v-model="message" />
</template>

<script>
export default {
  name: "HelloWorld",
  setup() {
    const message = "Mensaje Hello World";
    return {
      message,
    };
  },
};
</script>

<style>
</style>