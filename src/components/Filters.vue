<template>
  <div
    class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-2 lg:grid-cols-4 gap-4 mx-auto max-w-7x1 p-2 m-1"
  >
    <div>
      <p class="flex items-center text-gray-700 text-base mt-2 md:mt-0 md:text-center">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          fill="none"
          viewBox="0 0 24 24"
          stroke-width="1.5"
          stroke="currentColor"
          class="w-6 h-6"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            d="m2.25 12 8.954-8.955c.44-.439 1.152-.439 1.591 0L21.75 12M4.5 9.75v10.125c0 .621.504 1.125 1.125 1.125H9.75v-4.875c0-.621.504-1.125 1.125-1.125h2.25c.621 0 1.125.504 1.125 1.125V21h4.125c.621 0 1.125-.504 1.125-1.125V9.75M8.25 21h8.25"
          />
        </svg>

        Habitaciones
      </p>
      <label
        for="bedroom-1"
        class="ms-2 text-sm font-medium text-gray-900 dark:text-gray-300"
        >1</label
      >
      <input
        type="checkbox"
        id="bedroom-1"
        value="1"
        class="w-4 h-4 text-blue-600 bg-gray-100 border-gray-300 rounded focus:ring-blue-500 dark:focus:ring-blue-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600"
      />
      <label
        for="bedroom-2"
        class="ms-2 text-sm font-medium text-gray-900 dark:text-gray-300"
        >2</label
      >
      <input
        type="checkbox"
        id="bedroom-2"
        value="2"
        class="w-4 h-4 text-blue-600 bg-gray-100 border-gray-300 rounded focus:ring-blue-500 dark:focus:ring-blue-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600"
      />
    </div>
    <div>
      <p class="flex items-center text-gray-700 text-base mt-2 md:mt-0 md:text-center">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          fill="none"
          viewBox="0 0 24 24"
          stroke-width="1.5"
          stroke="currentColor"
          class="w-6 h-6"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            d="M15 19.128a9.38 9.38 0 0 0 2.625.372 9.337 9.337 0 0 0 4.121-.952 4.125 4.125 0 0 0-7.533-2.493M15 19.128v-.003c0-1.113-.285-2.16-.786-3.07M15 19.128v.106A12.318 12.318 0 0 1 8.624 21c-2.331 0-4.512-.645-6.374-1.766l-.001-.109a6.375 6.375 0 0 1 11.964-3.07M12 6.375a3.375 3.375 0 1 1-6.75 0 3.375 3.375 0 0 1 6.75 0Zm8.25 2.25a2.625 2.625 0 1 1-5.25 0 2.625 2.625 0 0 1 5.25 0Z"
          />
        </svg>

        Huéspedes
      </p>
      <label
        for="guest-2"
        class="ms-2 text-sm font-medium text-gray-900 dark:text-gray-300"
        >2</label
      >
      <input
        type="checkbox"
        id="guest-2"
        value="2"
        class="w-4 h-4 text-blue-600 bg-gray-100 border-gray-300 rounded focus:ring-blue-500 dark:focus:ring-blue-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600"
      />
      <label
        for="guest-3"
        class="ms-2 text-sm font-medium text-gray-900 dark:text-gray-300"
        >3</label
      >
      <input
        type="checkbox"
        id="guest-3"
        value="3"
        class="w-4 h-4 text-blue-600 bg-gray-100 border-gray-300 rounded focus:ring-blue-500 dark:focus:ring-blue-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600"
      />
      <label
        for="guest-4"
        class="ms-2 text-sm font-medium text-gray-900 dark:text-gray-300"
        >4</label
      >
      <input
        type="checkbox"
        id="guest-4"
        value="4"
        class="w-4 h-4 text-blue-600 bg-gray-100 border-gray-300 rounded focus:ring-blue-500 dark:focus:ring-blue-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600"
      />
    </div>
    <p class="flex items-center text-gray-700 md:mt-0 text-base mt-2 md:mt-0 md:text-center">
      <svg
        xmlns="http://www.w3.org/2000/svg"
        fill="none"
        viewBox="0 0 24 24"
        stroke-width="1.5"
        stroke="currentColor"
        class="w-6 h-6"
      >
        <path
          stroke-linecap="round"
          stroke-linejoin="round"
          d="M14.25 7.756a4.5 4.5 0 1 0 0 8.488M7.5 10.5h5.25m-5.25 3h5.25M21 12a9 9 0 1 1-18 0 9 9 0 0 1 18 0Z"
        />
      </svg>

      Precio
    </p>
    <div class="relative mb-2 md:justify-center">
      <label for="labels-range-input" class="sr-only">Labels range</label>
      <input
        id="labels-range-input"
        type="range"
        value="1000"
        min="1000"
        max="3000"
        class="w-full h-2 bg-gray-200 rounded-lg appearance-none cursor-pointer dark:bg-gray-700"
      />
      <span
        class="text-sm text-gray-500 dark:text-gray-400 absolute start-0 -bottom-6"
        >Min 2500</span
      >
      <span
        class="text-sm text-gray-500 dark:text-gray-400 absolute end-0 -bottom-6"
        >Max 3600</span
      >
    </div>
  </div>
</template>

<script></script>

<style>
.error-message {
  color: red;
  font-weight: bold;
}
</style>
