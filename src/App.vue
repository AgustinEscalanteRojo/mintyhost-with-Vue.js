<script>
import NavBar from "./components/NavBar.vue";
import BarrioSelector from "./components/BarrioSelector.vue";
import FilterModal from "./components/FilterModal.vue";
import ListApi from "./components/ListApi.vue";
import Filters from "./components/Filters.vue";

export default {
  data() {
    return {
      modalOpen: false,
    };
  },
  methods: {
    openModal() {
      this.modalOpen = true;
    },
    closeModal() {
      this.modalOpen = false;
    },
  },
  components: {
    NavBar,
    BarrioSelector,
    FilterModal,
    Filters,
    ListApi,
  },
};
</script>

<template>
  <NavBar />
  <BarrioSelector />
  <button
    @click="openModal"
    class="bg-blue-900 text-white py-2 px-4 rounded-md hover:bg-blue-800 min-w-80 mx-auto block"
  >
    Seleccionar filtros
  </button>
  <FilterModal :show="modalOpen" @close="closeModal">
    <Filters />
  </FilterModal>
  <ListApi />
</template>
