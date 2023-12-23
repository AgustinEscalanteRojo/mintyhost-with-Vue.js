<script>
import NavBar from "./components/NavBar.vue";
import Filters from "./components/Filters.vue";
import ListApi from "./components/ListApi.vue";

export default {
  components: {
    NavBar,
    Filters,
    ListApi,
  },
};
</script>

<template>
  <NavBar />
  <Filters />
  <ListApi />
</template>
