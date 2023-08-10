<template>
  <SimpleFetch />
  <hr />
  <TodoList />
  <hr />
  <SimpleCounterCompositionApi />
  <hr />
  <WatchCounter />
  <hr />
  <ReactiveCounter />
  <hr />
  <SimpleCounter />
  <hr />
  <HelloWorld />
</template>

<script>
import SimpleFetch from "@/components/06SimpleFetch";
import TodoList from "@/components/05TodoList";
import SimpleCounterCompositionApi from "@/components/04SimpleCounterCompositionApi";
import WatchCounter from "@/components/03WatchCounter";
import ReactiveCounter from "@/components/02ReactiveCounter";
import HelloWorld from "@/components/00HelloWorld";
import SimpleCounter from "@/components/01SimpleCounter";
import useTodos from "@/composables/useTodos";

export default {
  name: "Home",
  components: {
    HelloWorld,
    SimpleCounter,
    ReactiveCounter,
    WatchCounter,
    SimpleCounterCompositionApi,
    TodoList,
    SimpleFetch,
  },
  setup() {
    const { todo, todos, addTodo, deleteTodo } = useTodos();
    return { todo, todos, addTodo, deleteTodo };
  },
};
</script>
