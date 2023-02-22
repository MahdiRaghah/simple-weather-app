# Simple Weather App

This is a simple weather app that uses the OpenWeatherMap API to retrieve weather data for a user-specified location.

#### _Demo:_ [Click here](https://mahdiraghah-weather-app.pages.dev)

## Getting started

To use this app, you'll need an API key from OpenWeatherMap. You can obtain a free API key by creating an account on openweathermap.org and following the instructions to generate an API key.

Once you have an API key, replace the "{API_KEY}" placeholder in the script.js file with your actual API key.


```javascript
function requestApi(city) {
  api = `https://api.openweathermap.org/data/2.5/weather?q=${city}&units=metric&appid={API_KEY}`;
  fetchData();
}

function onSuccess(position) {
  const { latitude, longitude } = position.coords; // getting lat and lon of the user device from coords obj
  api = `https://api.openweathermap.org/data/2.5/weather?lat=${latitude}&lon=${longitude}&units=metric&appid={API_KEY}`;
  fetchData();
}
```

## Technologies used

This app was built using HTML, CSS, and JavaScript, and utilizes the OpenWeatherMap API for weather data.
