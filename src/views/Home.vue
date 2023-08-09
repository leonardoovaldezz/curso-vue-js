<template>
  <simple-counter-composition-api />
  <hr />
  <watch-counter />
  <hr />
  <reactive-counter />
  <hr />
  <simple-counter />
  <hr />
  <hello-world />
</template>

<script>
// @ is an alias to /src
import SimpleCounterCompositionApi from "@/components/04SimpleCounterCompositionApi";
import WatchCounter from "@/components/03WatchCounter";
import ReactiveCounter from "@/components/02ReactiveCounter";
import HelloWorld from "@/components/00HelloWorld";
import SimpleCounter from "@/components/01SimpleCounter";
export default {
  name: "Home",
  components: {
    HelloWorld,
    SimpleCounter,
    ReactiveCounter,
    WatchCounter,
    SimpleCounterCompositionApi,
  },
};
</script>
