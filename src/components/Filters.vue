<template>
  <div class="grid grid-cols-1 sm:grid-cols-1 md:grid-cols-1 lg:grid-cols-4 gap-4 mx-auto max-w-7x1 p-2 m-1">
    <div>
      <p class="text-gray-700 text-base mt-2">Bedrooms</p>
      <label for="bedroom-1">1</label>
      <input type="checkbox" id="bedroom-1" value="1" />
      <label for="bedroom-2">2</label>
      <input type="checkbox" id="bedroom-2" value="2" />
    </div>
    <div>
      <p class="text-gray-700 text-base mt-2">Guest</p>
      <label for="guest-2">2</label>
      <input type="checkbox" id="guest-2" value="2" />
      <label for="guest-3">3</label>
      <input type="checkbox" id="guest-3" value="3" />
      <label for="guest-4">4</label>
      <input type="checkbox" id="guest-4" value="4" />
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
// import axios from "axios";

// export default {
//   data() {
//     return {
//       apartments: [],
//       error: null,
//     };
//   },
//   methods: {
//     fetchData() {
//       const searchData = {
//         barrio_id: 1,
//         bedrooms: 2,
//         guests: 3,
//         min_price: 2999,
//         max_price: 3000,
//       };

//       axios
//         .post(
//           "https://api.dev.myplazze.com/api/v1/practice/search",
//           searchData,
//           {
//             headers: {
//               Accept: "application/json",
//               "Content-Type": "application/json",
//             },
//           }
//         )
//         .then((response) => {
//           console.log(response.data);
//           this.apartments = response.data;
//         })
//         .catch((error) => {
//           this.error = "Error fetching data: " + error.message;
//         });
//     },
//   },
//   mounted() {
//     this.fetchData();
//   },
// };
</script>

<style>
/* .apartment-card {
  border: 1px solid #ddd;
  padding: 10px;
  margin-bottom: 10px;
} */

.error-message {
  color: red;
  font-weight: bold;
}
</style>
