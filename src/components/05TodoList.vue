<template>
  <h2>Lista de Tareas</h2>
  <label for="todo">Todo</label>
  <input type="text" v-model="todo" @keypress.enter="addTodo" id="todo" />
  <ul>
    <li v-for="(t, index) in todos" :key="index">
      {{ t }} <span @click="deleteTodo(index)">X</span>
    </li>
  </ul>
</template>

<script>
import useTodos from "@/composables/useTodos";
export default {
  name: "TodoList",
  setup() {
    const { todo, todos, addTodo, deleteTodo } = useTodos();
    return { todo, todos, addTodo, deleteTodo };
  },
};
</script>

<style>
</style>