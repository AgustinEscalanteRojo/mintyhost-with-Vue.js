<template>
  <div>
    <div
      v-if="error"
      class="error-message bg-red-100 border-l-4 border-red-500 text-red-700 p-4 mb-4"
    >
      {{ error }}
    </div>

    <div
      v-if="apartments.length > 0"
      class="grid sm:grid-cols-1 md:grid-cols-2 lg:grid-cols-2 gap-1 mx-auto max-w-7xl p-4 m-4"
    >
      <div
        v-for="apartment in apartments"
        :key="apartment.id"
        class="bg-white overflow-hidden shadow-md rounded-md p-4"
      >
        <img
          class="w-full h-32 object-cover max-h-50 mb-4 rounded-md"
          :src="apartment.pic[1]"
          alt="Apartment"
        />

        <h2 class="text-gray-900 font-bold text-xl mb-2">
          {{ apartment.barrio.name }}
        </h2>
        <p class="text-gray-700 text-base">{{ apartment.apartment_title }}</p>
        <p class="flex items-center text-gray-700 text-base mt-2">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 24 24"
            stroke-width="1.5"
            stroke="currentColor"
            class="w-6 h-6 fill-yellow-500"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="m2.25 12 8.954-8.955c.44-.439 1.152-.439 1.591 0L21.75 12M4.5 9.75v10.125c0 .621.504 1.125 1.125 1.125H9.75v-4.875c0-.621.504-1.125 1.125-1.125h2.25c.621 0 1.125.504 1.125 1.125V21h4.125c.621 0 1.125-.504 1.125-1.125V9.75M8.25 21h8.25"
            />
          </svg>

          <strong>Habitaciones</strong> : {{ apartment.bedrooms }}
        </p>
        <p class="flex items-center text-gray-700 text-base mt-2">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 24 24"
            stroke-width="1.5"
            stroke="currentColor"
            class="w-6 h-6 fill-yellow-500"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="m20.25 7.5-.625 10.632a2.25 2.25 0 0 1-2.247 2.118H6.622a2.25 2.25 0 0 1-2.247-2.118L3.75 7.5M10 11.25h4M3.375 7.5h17.25c.621 0 1.125-.504 1.125-1.125v-1.5c0-.621-.504-1.125-1.125-1.125H3.375c-.621 0-1.125.504-1.125 1.125v1.5c0 .621.504 1.125 1.125 1.125Z"
            />
          </svg>

          <strong>Baños</strong> : {{ apartment.bathrooms }}
        </p>
        <p class="flex items-center text-gray-700 text-base mt-2">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 24 24"
            stroke-width="1.5"
            stroke="currentColor"
            class="w-6 h-6 fill-yellow-500"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M8.25 21v-4.875c0-.621.504-1.125 1.125-1.125h2.25c.621 0 1.125.504 1.125 1.125V21m0 0h4.5V3.545M12.75 21h7.5V10.75M2.25 21h1.5m18 0h-18M2.25 9l4.5-1.636M18.75 3l-1.5.545m0 6.205 3 1m1.5.5-1.5-.5M6.75 7.364V3h-3v18m3-13.636 10.5-3.819"
            />
          </svg>

          <strong>Ciudad</strong> : {{ apartment.town }}
        </p>
        <p class="flex items-center text-gray-700 text-base mt-2">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 24 24"
            stroke-width="1.5"
            stroke="currentColor"
            class="w-6 h-6 fill-yellow-500"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M8.288 15.038a5.25 5.25 0 0 1 7.424 0M5.106 11.856c3.807-3.808 9.98-3.808 13.788 0M1.924 8.674c5.565-5.565 14.587-5.565 20.152 0M12.53 18.22l-.53.53-.53-.53a.75.75 0 0 1 1.06 0Z"
            />
          </svg>

          <strong>Servicios</strong> : {{ apartment.amenities }}
        </p>
        <p class="flex items-center text-gray-700 text-base mt-2">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 24 24"
            stroke-width="1.5"
            stroke="currentColor"
            class="w-6 h-6 fill-yellow-500"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M14.25 7.756a4.5 4.5 0 1 0 0 8.488M7.5 10.5h5.25m-5.25 3h5.25M21 12a9 9 0 1 1-18 0 9 9 0 0 1 18 0Z"
            />
          </svg>

          <strong>Precio</strong> : {{ apartment.monthly_price }}
        </p>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  data() {
    return {
      apartments: [],
      error: null,
    };
  },
  methods: {
    fetchData() {
      const searchData = {
        barrio_id: 1,
        bedrooms: 2,
        guests: 3,
        min_price: 2999,
        max_price: 3000,
      };

      axios
        .post("https://api.dev.myplazze.com/api/v1/practice/search", {
          headers: {
            Accept: "application/json",
            "Content-Type": "application/json",
          },
        })
        .then((response) => {
          console.log(response.data);
          this.apartments = response.data;
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
.apartment-card {
  border: 1px solid #ddd;
  padding: 10px;
  margin-bottom: 20px;
}

.error-message {
  color: red;
  font-weight: bold;
}
</style>
