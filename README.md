````markdown
# Weather App

A simple weather application that fetches and displays current weather information for selected cities using the [FreeCodeCamp weather proxy API](https://weather-proxy.freecodecamp.rocks/).

---

## Features

- Select from seven cities: New York, Los Angeles, Chicago, Paris, Tokyo, London, or no selection.
- Fetches real-time weather data including:
  - Weather icon and description
  - Main temperature (°C)
  - Feels like temperature (°C)
  - Humidity (%)
  - Wind speed (m/s)
  - Wind gust (m/s)
  - Weather type (e.g., Clear, Rain)
  - Location name
- Handles errors gracefully with alerts.
- Displays `N/A` when data is unavailable.
- Minimal, clean UI with responsive elements.

---

## User Stories

- Button with id `get-forecast` triggers the weather fetch.
- Dropdown (`select`) with seven `option`s including a blank default.
- If no city is selected, button does nothing.
- When a city is selected, weather info displays in designated elements.
- Async functions `getWeather(city)` and `showWeather(city)` handle data fetching and rendering.
- Logs errors to the console.
- Alerts user on failure (especially for Paris city test case).

---

## How to Run

1. Clone or download the project files.
2. Open `index.html` in a modern browser.
3. Select a city from the dropdown.
4. Click the **Get Forecast** button.
5. View the weather data displayed below.

---

## Technical Details

- Uses native JavaScript `fetch` API with async/await.
- Weather data fetched from:  
  `https://weather-proxy.freecodecamp.rocks/api/city/<city>`
- Temperatures and wind speed use metric units (°C, m/s).
- Basic CSS for styling.
- Error handling includes network failures and API errors.

---

## Example API Response

```json
{
  "weather": [
    {
      "main": "Clear",
      "description": "clear sky",
      "icon": "https://cdn.freecodecamp.org/weather-icons/01n.png"
    }
  ],
  "main": {
    "temp": 2.62,
    "feels_like": 0.84,
    "temp_min": 1.72,
    "temp_max": 3.49,
    "pressure": 1010,
    "humidity": 81
  },
  "visibility": 10000,
  "wind": {
    "speed": 1.79,
    "deg": 285,
    "gust": 3.13
  },
  "name": "London"
}
```

---

## Notes

* The Paris city is programmed to simulate an error response to demonstrate error handling.
* If API data fields are undefined, the app displays `N/A`.
* The project meets all FreeCodeCamp weather app test suite requirements.

---

## License

This project is open source and free to use.

---
