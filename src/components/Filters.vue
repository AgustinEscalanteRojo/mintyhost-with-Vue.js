<template>
  <div class="grid grid-cols-1 sm:grid-cols-1 md:grid-cols-1 lg:grid-cols-4 gap-4 mx-auto max-w-7x1 p-2 m-1">
    <div>
      <p class="text-gray-700 text-base mt-2">Bedrooms</p>
      <label for="bedroom-1" class="ms-2 text-sm font-medium text-gray-900 dark:text-gray-300">1</label>
      <input type="checkbox" id="bedroom-1" value="1" class="w-4 h-4 text-blue-600 bg-gray-100 border-gray-300 rounded focus:ring-blue-500 dark:focus:ring-blue-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600"/>
      <label for="bedroom-2" class="ms-2 text-sm font-medium text-gray-900 dark:text-gray-300">2</label>
      <input type="checkbox" id="bedroom-2" value="2" class="w-4 h-4 text-blue-600 bg-gray-100 border-gray-300 rounded focus:ring-blue-500 dark:focus:ring-blue-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600"/>
    </div>
    <div>
      <p class="text-gray-700 text-base mt-2">Guest</p>
      <label for="guest-2" class="ms-2 text-sm font-medium text-gray-900 dark:text-gray-300">2</label>
      <input type="checkbox" id="guest-2" value="2" class="w-4 h-4 text-blue-600 bg-gray-100 border-gray-300 rounded focus:ring-blue-500 dark:focus:ring-blue-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600" />
      <label for="guest-3" class="ms-2 text-sm font-medium text-gray-900 dark:text-gray-300">3</label>
      <input type="checkbox" id="guest-3" value="3" class="w-4 h-4 text-blue-600 bg-gray-100 border-gray-300 rounded focus:ring-blue-500 dark:focus:ring-blue-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600"/>
      <label for="guest-4" class="ms-2 text-sm font-medium text-gray-900 dark:text-gray-300">4</label>
      <input type="checkbox" id="guest-4" value="4" class="w-4 h-4 text-blue-600 bg-gray-100 border-gray-300 rounded focus:ring-blue-500 dark:focus:ring-blue-600 dark:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600" />
    </div>
    <p class="text-gray-700 text-base mt-2">Price</p>
    <div class="relative mb-2">
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
        >Min 2900</span
      >
      <span
        class="text-sm text-gray-500 dark:text-gray-400 absolute end-0 -bottom-6"
        >Max 3000</span
      >
    </div>
  </div>
</template>

<script>

</script>

<style>

.error-message {
  color: red;
  font-weight: bold;
}
</style>
