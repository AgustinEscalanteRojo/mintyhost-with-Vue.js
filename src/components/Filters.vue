<template>
  <div>
    <BarrioSelect :barrios="barrios" @selectBarrio="updateBarrio" />
    <FilterModal
      v-if="showModal"
      @closeModal="closeModal"
      @applyFilters="applyFilters"
    />
    <SearchButton @click="performSearch" />
  </div>
</template>

<script>
import BarrioSelect from '@/components/BarrioSelect.vue';
import FilterModal from '@/components/FilterModal.vue';
import SearchButton from '@/components/SearchButton.vue';

export default {
  data() {
    return {
      barrios: ["Barrio 1", "Barrio 2", "Barrio 3"], // Ejemplo de datos para los barrios
      showModal: false,
      selectedBarrio: null,
      // Otros datos para los filtros como precio, dormitorios, capacidad, etc.
    };
  },
  methods: {
    updateBarrio(barrio) {
      this.selectedBarrio = barrio;
    },
    openModal() {
      this.showModal = true;
    },
    closeModal() {
      this.showModal = false;
    },
    applyFilters(filters) {
      // Lógica para aplicar los filtros (precio, dormitorios, capacidad, etc.)
      console.log(filters);
      this.closeModal();
    },
    performSearch() {
      // Lógica para realizar la búsqueda con los filtros seleccionados
      console.log("Realizando búsqueda...");
      console.log("Barrio:", this.selectedBarrio);
      // Otras variables de filtros aquí...
    },
  },
  components: {
    BarrioSelect,
    FilterModal,
    SearchButton,
  },
};
</script>
