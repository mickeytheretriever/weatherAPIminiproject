**Portugal Weather Forecast Project**
This project fetches, processes, and summarizes 7-day weather forecast data for five major Portuguese cities (Lisbon, Porto, Braga, Faro, Evora) using the Open-Meteo API.

Features:
**Data Acquisition:** Downloads daily weather forecast data (temperatures, precipitation, wind speed, weather codes) for the next 7 days.
**Temperature Conversion:** Converts daily maximum and minimum temperatures from Celsius to Fahrenheit.
**Weather Interpretation:** Translates WMO weather codes into descriptive "Expected Weather" conditions.
**Weekly Summary Report:** Generates a weekly_weather_report DataFrame, providing a consolidated view of each city's weekly maximum/minimum temperatures, total precipitation/rain, maximum wind speed, and the most common expected weather.
**Data Export:** Exports both the detailed weather_data and the summarized weekly_weather_report into separate CSV files for further analysis or use.
