# Portugal Weather Forecast Project

This project fetches, processes, and summarizes 7-day **weather forecast data** for five major Portuguese cities (Lisbon, Porto, Braga, Faro, Evora) using the **Open-Meteo API**.

## Features:

### Data Acquisition:
Downloads daily weather forecast data (temperatures, precipitation, wind speed, weather codes) for the next 7 days.

### Temperature Conversion:
Converts daily maximum and minimum temperatures from Celsius to Fahrenheit.

### Weather Interpretation:
Translates WMO weather codes into descriptive "Expected Weather" conditions.

### Weekly Summary Report:
Generates a weekly_weather_report DataFrame, providing a consolidated view of each city's weekly maximum/minimum temperatures, total precipitation/rain, maximum wind speed, and the most common expected weather.

### Data Export:
Exports both the detailed weather_data and the summarized weekly_weather_report into separate CSV files for further analysis or use.

# Project structure: 

- **cities (Dictionary):** Stores the names of the major Portuguese cities along with their latitude and longitude coordinates. This is used to make API calls for each specific city.

- **today, tomorrow, end_date (Date Objects):** These variables are used to dynamically calculate the 7-day forecast period. today is the current date, tomorrow is the day after today, and end_date marks the end of the 7-day forecast starting from tomorrow.

- **BASE_URL (String)**: The base URL for the Open-Meteo API endpoint, used for fetching weather forecast data.

- **params (Dictionary):** Contains the general parameters required for the API request, such as the daily weather variables to fetch (temperature_2m_max, precipitation_sum, etc.), timezone, and the start_date and end_date for the forecast.

- **all_weather_data (List of DataFrames):** An empty list initialized to store individual pandas DataFrames. Each DataFrame will contain the weather data for a single city during the forecast period. These are later concatenated into a single DataFrame.

 -**weather_data (pandas DataFrame):** This is the main DataFrame that consolidates all the fetched daily weather data for all cities after concatenating the DataFrames from all_weather_data.

- **get_weather_description(code) (Function):** A user-defined function that takes a Weather Code (an integer) as input and returns a human-readable string description of the weather condition (e.g., "Clear sky", "Moderate rain").

- **weekly_weather_report (pandas DataFrame):** A summary DataFrame created by grouping the weather_data by city and calculating weekly aggregates. It includes the weekly maximum and minimum temperatures, total precipitation and rain, maximum wind speed, and the most frequent weather condition (mode) for each city.
