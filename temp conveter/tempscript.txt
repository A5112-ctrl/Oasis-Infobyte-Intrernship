function convertTemperature() {
    var temperatureInput = document.getElementById("temperature").value;
    var unit = document.getElementById("unit").value;
    var resultElement = document.getElementById("result");

    if (temperatureInput === "") {
        alert("Please enter a temperature value.");
        return;
    }

    var temperature = parseFloat(temperatureInput);
    var convertedTemperature;

    if (unit === "celsius") {
        // Convert Celsius to Fahrenheit
        convertedTemperature = (temperature * 9/5) + 32;
        resultElement.textContent = temperature + "°C is equal to " + convertedTemperature.toFixed(2) + "°F.";
    } else {
        // Convert Fahrenheit to Celsius
        convertedTemperature = (temperature - 32) * 5/9;
        resultElement.textContent = temperature + "°F is equal to " + convertedTemperature.toFixed(2) + "°C.";
    }
}
