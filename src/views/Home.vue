<template>
  <simple-counter />
  <hr />
  <hello-world />
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/00HelloWorld";
import SimpleCounter from "@/components/01SimpleCounter";
export default {
  name: "Home",
  components: {
    HelloWorld,
    SimpleCounter,
  },
};
</script>
