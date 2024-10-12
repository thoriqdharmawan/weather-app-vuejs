# ☀️ Weather App

A simple and beautiful weather app built with Vue.js, powered by **Mapbox** for place search and **OpenWeather** for weather data. You can easily search for any city's weather, get up-to-date information, and even save your favorite cities! 🌍🌦️

<p align="center">
  <img src="https://github.com/user-attachments/assets/794d149a-f701-4bfc-a8b6-ed15e9ddb9a2" alt="screenshot1" width="45%" style="margin-right: 12px;" />
  <img src="https://github.com/user-attachments/assets/18404663-8776-4549-89e4-92b4e345488b" alt="screenshot2" width="45%" />
</p>

## ✨ Features

- 🔍 **Search Locations with Mapbox**: Easily search for locations by name using Mapbox's powerful place search.
- ☁️ **Real-time Weather Information**: Get the latest weather data for any city from OpenWeather.
- 💾 **Save Favorite Cities**: Store and manage your favorite cities for quick access.

## 🛠️ Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/thoriqdharmawan/weather-app-vuejs.git
   cd weather-app
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Create a `.env` file in the root of your project and add your API keys for Mapbox and OpenWeather:

   ```bash
   VITE_OPEN_WEATHER_API_KEY=your_mapbox_api_key
   VITE_MAPBOX_API_KEY=your_openweather_api_key
   ```

4. Run the app in development mode:

   ```bash
   npm run dev
   ```

5. Build the app for production:

   ```bash
   npm run build
   ```

6. Preview the production build:
   ```bash
   npm run preview
   ```

## 🧑‍💻 Technologies Used

- [Vue.js](https://vuejs.org/) 🖼️: Frontend framework
- [Tailwind CSS](https://tailwindcss.com/) 🎨: Utility-first CSS framework
- [Vite](https://vitejs.dev/) ⚡: Fast development build tool
- [Mapbox API](https://www.mapbox.com/) 🗺️: Location search service
- [OpenWeather API](https://openweathermap.org/) 🌤️: Weather information service

## 📦 Dependencies

- **axios**: For making API requests
- **vue-router**: For handling app routing
- **uid**: For generating unique IDs
