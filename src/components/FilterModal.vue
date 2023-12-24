<template>
  <div
    v-if="show"
    class="fixed inset-0 flex items-center justify-center bg-black bg-opacity-50"
  >
  <div class="bg-white p-4 rounded-md sm:w-full md:w-1/2">
      <div class="mt-2 flex justify-end flex-col sm:flex-row">
        <slot></slot>
        <div>
          <button
          @click="closeModal"
          class="px-1 py-2 mt-2 bg-blue-900 text-white rounded-md hover:bg-black-700 focus:outline-none sm:mr-2 sm:mb-2"
          >
            Aceptar
          </button>
        </div>
        <div>
          <button
            @click="closeModal"
            class="px-1 py-2 mt-2 bg-blue-900 text-white rounded-md hover:bg-black-700 focus:outline-none sm:mr-2 sm:mb-2"
          >
            Cerrar
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    show: Boolean,
  },
  methods: {
    closeModal() {
      this.$emit("close");
    },
  },
};
</script>
