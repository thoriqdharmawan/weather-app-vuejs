<template>
  <div v-for="city in savedCities" :key="city.id">
    <CityCard :city="city" @click="goToCityView(city)" />
  </div>

  <p v-if="savedCities.length === 0">
    No locations added. To start tracking a location, search in
    the field above.
  </p>
</template>

<script setup>
import axios from 'axios';
import { ref } from 'vue';
import CityCard from './CityCard.vue';
import { useRouter } from 'vue-router';

const router = useRouter()

const savedCities = ref([])
const getCities = async () => {
  if (localStorage.getItem("savedCities")) {
    savedCities.value = JSON.parse(localStorage.getItem("savedCities"))

    const request = [];
    savedCities.value.forEach((city) => {
      request.push(
        axios.get(
          `https://api.openweathermap.org/data/2.5/weather`, {
          params: {
            lat: city.coords?.lat,
            lon: city.coords?.lng,
            appid: import.meta.env.VITE_OPEN_WEATHER_API_KEY,
            units: 'metric'
          }
        })
      )
    })

    const weatherData = await Promise.all(request)

    weatherData.forEach((value, index) => {
      savedCities.value[index].weather = value.data
    })
  }
}

await getCities()

const goToCityView = (city) => {
  router.push({
    name: "cityView",
    params: { state: city.state, city: city.city },
    query: {
      id: city.id,
      lat: city.coords.lat,
      lng: city.coords.lng,
    },
  });
};
</script>