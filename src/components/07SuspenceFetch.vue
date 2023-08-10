<template>
  <h2>Suspense Fetch</h2>
  <ul v-if="users">
    <li v-for="user in users" :key="user.id">
      {{ user.name }} - {{ user.email }}
    </li>
  </ul>
</template>
    
  <script>
import { ref, onMounted } from "vue";
export default {
  name: "SuspenseFetch",
  async setup() {
    const users = ref(null);

    const fetchData = async () => {
      const response = await fetch(
        "https://jsonplaceholder.typicode.com/users"
      );
      return new Promise((resolve) => {
        setTimeout(() => {
          resolve(response.json());
        }, 5000);
      });
    };

    onMounted(async () => {
      users.value = await fetchData();
    });

    return { users };
  },
};
</script>
    
    <style>
</style>
  