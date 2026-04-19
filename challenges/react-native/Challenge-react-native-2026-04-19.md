# Challenge: React Native Weather Dashboard

## Difficulty
Medium

## Description
Create a cross‑platform mobile application using **React Native** that displays real‑time weather information for the user's current location and allows the user to search for weather data in other cities. The app should feature a clean, responsive UI and handle various edge cases such as network errors and permission denials.

## Requirements
- **Location Access**
  - Prompt the user for location permissions.
  - Retrieve the device’s current latitude and longitude.
- **Weather Data**
  - Use a public weather API (e.g., OpenWeatherMap) to fetch current weather data based on coordinates or city name.
  - Display at minimum: temperature, weather condition (e.g., sunny, rainy), humidity, wind speed, and an appropriate weather icon.
- **Search Functionality**
  - Provide a text input where the user can type a city name.
  - On submission, fetch and display the weather for the entered city.
- **UI Design**
  - Create a visually appealing home screen showing the current location’s weather.
  - Include a separate screen or modal for displaying search results.
  - Ensure the layout works on both iOS and Android devices of various screen sizes.
- **State Management**
  - Manage loading states, error states, and successful data retrieval using React hooks or a state‑management library (e.g., Redux, Zustand).
- **Error Handling**
  - Gracefully handle scenarios such as:
    - No internet connection.
    - Denied location permissions.
    - Invalid city names or API errors.
  - Show user‑friendly error messages.

## Bonus
- Implement a pull‑to‑refresh gesture to update the weather data.
- Cache the last successful weather data locally (e.g., using AsyncStorage) and display it when the app launches offline.
- Add a toggle for switching between Celsius and Fahrenheit.
- Use animations (e.g., fade‑in weather icons, smooth transitions between screens) to enhance user experience.
- Support dark mode by adapting UI colors based on the device’s theme setting.