---
name: open-weather-city
description: Get current weather and forecast for any city by name using OpenWeatherMap.
metadata:
  require-secret: true
  require-secret-description: Paste your OpenWeatherMap API Key here.
---

# Weather by City Name

## Instructions

When the user asks about the weather in a specific place:

Call the `run_js` tool with the following exact parameters:

- script name: index.html
- data: A JSON string with the following fields:
  - city: String. The name of the city (e.g., "Guamúchil", "New York,US").
  - units: String. Either "metric" (Celsius) or "imperial" (Fahrenheit). Default to "metric".