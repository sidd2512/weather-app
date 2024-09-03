
 [WEATHER APP LINK](#https://weather-app-siddharth.netlify.app/)
 
 
 # Weather App Documentation

## Project Overview
This weather app allows users to check the current weather in their location or any other city by either granting location access or searching for a city manually. The application fetches weather data from the OpenWeatherMap API and displays key weather information such as temperature, wind speed, humidity, and cloud coverage.

## Technologies Used
- **HTML**: Structure of the app's interface.
- **CSS**: Styling of the interface for a clean and modern look.
- **JavaScript**: Handles the logic for fetching and displaying weather data.
- **OpenWeatherMap API**: Provides real-time weather data.

## Features
1. **Two Weather Modes**:
   - **Your Weather**: Displays the weather of the user's current location by using the browser's geolocation API.
   - **Search Weather**: Allows users to search for weather information by city name.

2. **Weather Information Display**:
   - City name and country flag.
   - Weather description and icon.
   - Temperature in Celsius.
   - Wind speed, humidity, and cloud coverage.

3. **Error Handling**:
   - Handles errors like invalid city names or denied location access by displaying appropriate error messages.

4. **Loading State**:
   - Shows a loading animation while fetching weather data to enhance user experience.

## JavaScript Implementation (script.js)

### API Key
- The API key for OpenWeatherMap is stored in a constant `API_KEY`.

### Tab Switching
- The app has two main tabs, "Your Weather" and "Search Weather".
- The `switchTab` function handles switching between these tabs, ensuring that only the relevant tab content is visible.

### Fetching Weather Data
1. **Your Weather**:
   - The app attempts to fetch the user's coordinates from the session storage.
   - If coordinates are not found, it prompts the user to grant location access.
   - Upon granting access, the browser’s geolocation API retrieves the user's coordinates, which are then used to fetch weather data from the API.

2. **Search Weather**:
   - Users can input a city name into the search form.
   - The `fetchSearchWeatherInfo` function is called on form submission, which sends a request to the API with the city name and displays the corresponding weather data.

### Rendering Weather Data
- The `renderWeatherInfo` function updates the UI with the fetched weather data, including city name, country flag, temperature, wind speed, humidity, and cloud coverage.

### Error Handling
- The app includes error handling to manage cases where the API fails to return valid data. If an error occurs (e.g., invalid city name or network issues), the app displays an error message in the UI.

### Session Storage
- The app uses session storage to save and retrieve the user's coordinates, allowing quick access to weather information without requiring the user to grant location access every time they revisit the app.

