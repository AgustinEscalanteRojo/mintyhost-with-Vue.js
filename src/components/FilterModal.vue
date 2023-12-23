<template>
  <div
    v-if="show"
    class="fixed inset-0 flex items-center justify-center bg-black bg-opacity-50"
  >
    <div class="bg-white p-4 rounded-md w-1/2">
      <div class="mt-2 flex justify-end">
        <slot></slot>
        <div>
          <button
          @click="closeModal"
            class="px-6 py-2 bg-blue-900 text-white rounded-md hover:bg-black-700 focus:outline-none"
          >
            Aceptar
          </button>
        </div>
        <div>
          <button
            @click="closeModal"
            class="px-6 py-2 bg-blue-900 text-white rounded-md hover:bg-black-700 focus:outline-none"
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
