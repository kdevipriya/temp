# temp
<!DOCTYPE html>
<html>
<head>
  <title>Temperature Converter</title>
  <link rel="stylesheet" type="text/css" href="temp glo1.css">
</head>
<body>
<img src="C:\Users\konda\Downloads\ddd.png">
  <h1>TEMPERATURE CONVERTER</h1>
  
  <div class="converter">
    <input type="number" id="temperatureInput" placeholder="Enter temperature" required>
    <select id="unitSelect">
      <option value="celsius">Celsius</option>
      <option value="fahrenheit">Fahrenheit</option>
      <option value="kelvin">Kelvin</option>
    </select>
    <button onclick="convertTemperature()">Convert</button>
    <div id="resultArea"></div>
  </div>

  <script src="tej.js"></script>
</body>
</html>

/* Global Styles */
body {
  font-family: Arial, sans-serif;
  margin: 50px;
  padding: 20;
}

body{
background-color: lightblue;
<img src="C:\Users\konda\Downloads\ddd.png" >
background-image: url("ddd.png");
}

h1 {
  text-align: center;
}

.converter {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
  max-width: 500px;
  margin: 0 auto;
  padding: 20px;
  background-color: white;
}
function convertTemperature() {
  const temperatureInput = document.getElementById("temperatureInput");
  const unitSelect = document.getElementById("unitSelect");
  const resultArea = document.getElementById("resultArea");
  
  const temperature = parseFloat(temperatureInput.value);
  const unit = unitSelect.value;
  
  let convertedTemperature;
  let convertedUnit;
  
  if (unit === "celsius") {
    convertedTemperature = (temperature * 9/5) + 32;
    convertedUnit = "Fahrenheit";
  } else if (unit === "fahrenheit") {
    convertedTemperature = (temperature - 32) * 5/9;
    convertedUnit = "Celsius";
  } else if (unit === "kelvin") {
    convertedTemperature = temperature + 273.15;
    convertedUnit = "Kelvin";
  }
  
  resultArea.innerHTML = `${convertedTemperature.toFixed(2)} ${convertedUnit}`;
}


