# Temperature-Conversion 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Temperature Converter</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            padding: 20px;
            background: #f4f4f9;
        }

        h1 {
            color: #333;
        }

        input[type="number"] {
            padding: 10px;
            margin: 10px;
            width: 200px;
            font-size: 16px;
        }

        button {
            padding: 10px 20px;
            margin: 10px;
            background-color: #4CAF50;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 16px;
        }

        button:hover {
            background-color: #45a049;
        }

        .output {
            margin-top: 20px;
            font-size: 20px;
            color: #444;
        }
    </style>
</head>
<body>
    <h1>Temperature Converter</h1>

    <!-- Celsius to Fahrenheit -->
    <input type="number" id="inputCelsius" placeholder="Enter Celsius">
    <button onclick="convertToFahrenheit()">Convert to Fahrenheit</button>

    <!-- Fahrenheit to Celsius -->
    <input type="number" id="inputFahrenheit" placeholder="Enter Fahrenheit">
    <button onclick="convertToCelsius()">Convert to Celsius</button>

    <!-- Reset Button -->
    <button onclick="resetFields()">Reset</button>

    <!-- Output Section -->
    <div class="output" id="outputResult"></div>

    <script>
        // Convert Celsius to Fahrenheit
        function convertToFahrenheit() {
            var celsius = document.getElementById("inputCelsius").value;
            if (celsius !== "") {
                var fahrenheit = (parseFloat(celsius) * 9/5) + 32;
                document.getElementById("outputResult").innerHTML = 
                    celsius + "°C = " + fahrenheit.toFixed(2) + "°F";
            } else {
                alert("Please enter a Celsius value.");
            }
        }

        // Convert Fahrenheit to Celsius
        function convertToCelsius() {
            var fahrenheit = document.getElementById("inputFahrenheit").value;
            if (fahrenheit !== "") {
                var celsius = (parseFloat(fahrenheit) - 32) * 5/9;
                document.getElementById("outputResult").innerHTML = 
                    fahrenheit + "°F = " + celsius.toFixed(2) + "°C";
            } else {
                alert("Please enter a Fahrenheit value.");
            }
        }

        // Reset all fields
        function resetFields() {
            document.getElementById("inputCelsius").value = "";
            document.getElementById("inputFahrenheit").value = "";
            document.getElementById("outputResult").innerHTML = "";
        }
    </script>
</body>
</html>
