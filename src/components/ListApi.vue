<template>
  <div>
    <div v-if="error" class="error-message bg-red-100 border-l-4 border-red-500 text-red-700 p-4 mb-4">
      {{ error }}
    </div>

    <div v-if="apartments.length > 0" class="grid grid-cols-1 sm:grid-cols-1 md:grid-cols-1 lg:grid-cols-1 gap-1 mx-auto max-w-7xl p-4 m-4">
      <div v-for="apartment in apartments" :key="apartment.id" class="bg-white overflow-hidden shadow-md rounded-md p-4">
        <img class="w-full h-32 object-cover max-h-50 mb-4 rounded-md" :src="apartment.pic[1]" alt="Apartment">
        <h2 class="text-gray-900 font-bold text-xl mb-2">{{ apartment.barrio.name }}</h2>
        <p class="text-gray-700 text-base">{{ apartment.apartment_title }}</p>
        <p class="text-gray-700 text-base mt-2">Bedrooms: {{ apartment.bedrooms }}</p>
        <p class="text-gray-700 text-base mt-2">Bathrooms: {{ apartment.bathrooms }}</p>
        <p class="text-gray-700 text-base mt-2">Bedrooms: {{ apartment.town }}</p>
        <p class="text-gray-700 text-base mt-2">Amenities: {{ apartment.amenities }}</p>
        <p class="text-gray-700 text-base mt-2">Monthly Price: {{ apartment.monthly_price }}</p>

      </div>
    </div>
  </div>

</template>

<script>
import axios from 'axios';

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

      axios.post('https://api.dev.myplazze.com/api/v1/practice/search', searchData, {
        headers: {
          Accept: 'application/json',
          'Content-Type': 'application/json',
        },
      })
      .then(response => {
        console.log(response.data)
        this.apartments = response.data;
      })
      .catch(error => {
        this.error = 'Error fetching data: ' + error.message;
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
  margin-bottom: 10px;
}

.error-message {
  color: red;
  font-weight: bold;
}
</style>