<template>
  <hello-world />
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/00HelloWorld";

export default {
  name: "Home",
  components: {
    HelloWorld,
  },
};
</script>
