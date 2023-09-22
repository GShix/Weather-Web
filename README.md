# Project 1: Weather Web App

Certainly! Here's a detailed explanation of the HTML and JavaScript code that I have used:

**HTML Structure:**

1. `<!DOCTYPE html>`: This declaration specifies that the document follows the HTML5 standard.

2. `<html lang="en">`: This opening tag defines the root of the HTML document and indicates that the document is written in English.

3. `<head>`: This section contains metadata about the document, including character encoding, viewport settings, and the title of the page. It also links an external CSS file named "style.css."

4. `<body>`: This section contains the visible content of the webpage.

**Page Content:**

5. `<div class="card">`: This `<div>` element with the class "card" appears to be used as a container for the weather app's content.

   - Inside the "card," there are several sections:

     - `<div class="search">`: This `<div>` contains an input field for entering a city name and a button with a search icon.
       - `<input type="text" placeholder="Enter City Name" spellcheck="false">`: An input field where the user can enter a city name. The "spellcheck" attribute is set to "false" to disable spell checking.
       - `<button><img src="search.png"></button>`: A button with an embedded image (a search icon).

     - `<div class="invalidCity">`: This `<div>` is initially hidden and is used to display an "Invalid City Name" message if the user enters an invalid city.

     - `<div class="main">`: This `<div>` displays weather information.
       - `<img class="main-icon" src="rain.png">`: An image, presumably representing the weather conditions. The initial image is "rain.png."
       - `<h1 class="temp">20°c</h1>`: The current temperature, displayed as text.
       - `<h2 class="city">Nepalgunj</h2>`: The city name, initially set to "Nepalgunj."
       - `<div class="detail">`: This `<div>` contains additional weather details displayed in two columns.
         - Inside each column (`<div class="col">`):
           - An image representing either humidity or wind speed.
           - Text displaying the percentage of humidity or wind speed.

**JavaScript:**

6. The JavaScript code block enclosed in `<script>` tags contains the following functionality:

   - It defines a constant `apiUrl` with the URL for fetching weather data from the OpenWeatherMap API. The API key and units (metric) are included in the URL.

   - It selects various HTML elements, such as the search input field, search button, and the main weather icon, and assigns them to variables (`searchBox`, `searchBtn`, and `mainIcon`, respectively).

   - It defines an `async` function named `checkWeather(city)` to fetch weather data based on the provided city name and update the displayed weather information.

   - Inside `checkWeather(city)`, it fetches weather data from the API and checks if the response status is 404 (indicating an invalid city). If it's an invalid city, it displays the "Invalid City Name" message and hides the weather details. If it's a valid city, it updates the weather information and displays it.

   - The script also updates the main weather icon based on the weather conditions reported by the API. Different images are used for various weather conditions (e.g., "clouds.png" for cloudy weather).

   - Finally, it displays the weather details (`main` section) after a successful input.

   - An event listener is added to the search button, so when the button is clicked, it calls the `checkWeather` function with the value entered in the `searchBox` input field as the city name.

In summary, this code creates a simple weather app interface where users can enter a city name, click the search button, and see the current weather details displayed on the page. If the entered city is invalid, it shows an error message.