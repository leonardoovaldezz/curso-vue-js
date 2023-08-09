<template>
  <reactive-counter />
  <hr />
  <simple-counter />
  <hr />
  <hello-world />
</template>

<script>
// @ is an alias to /src
import ReactiveCounter from "@/components/02ReactiveCounter";
import HelloWorld from "@/components/00HelloWorld";
import SimpleCounter from "@/components/01SimpleCounter";
export default {
  name: "Home",
  components: {
    HelloWorld,
    SimpleCounter,
    ReactiveCounter,
  },
};
</script>
