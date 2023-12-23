<template>
  <div
    class="grid grid-cols-1 sm:grid-cols-1 md:grid-cols-1 lg:grid-cols-1 gap-1 mx-auto max-w-7xl p-4 m-4"
  >
    <label
      for="barrio"
      class="block mb-2 text-sm font-medium text-gray-900 dark:text-white"
      >Barrios</label
    >
    <select
      id="barrio"
      class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-900 focus:border-blue-900 block w-full p-2.5 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-900 dark:focus:border-blue-900"
    >
      <option selected>Selecciona un barrio</option>
      <option v-for="barrio in barrios" :key="barrio.id">
        {{ barrio.name }}
      </option>
    </select>
  </div>
</template>

<script>
import axios from "axios";

export default {
  data() {
    return {
      barrios: [],
      error: null,
    };
  },
  methods: {
    fetchData() {
      axios
        .get("https://api.dev.myplazze.com/api/v1/practice/barrios", {
          header: {
            Accept: "application/json",
          },
        })
        .then((response) => {
          console.log(response.data);
          this.barrios = response.data;
        })
        .catch((error) => {
          this.error = "Error fetching data: " + error.message;
        });
    },
  },
  mounted() {
    this.fetchData();
  },
};
</script>

<style>
.error-message {
  color: red;
  font-weight: bold;
}
</style>
