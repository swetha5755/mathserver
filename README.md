# Ex.05 Design a Website for Server Side Processing
# Date:10.12.2024
# AIM:
To design a website to calculate the power of a lamp filament in an incandescent bulb in the server side.

# FORMULA:
P = I2R
P --> Power (in watts)
 I --> Intensity
 R --> Resistance

# DESIGN STEPS:
## Step 1:
Clone the repository from GitHub.

## Step 2:
Create Django Admin project.

## Step 3:
Create a New App under the Django Admin project.

## Step 4:
Create python programs for views and urls to perform server side processing.

## Step 5:
Create a HTML file to implement form based input and output.

## Step 6:
Publish the website in the given URL.

# PROGRAM :
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Incandescent Bulb Power Calculator</title>
    <style>
        body {
            background-image: url(https://i.pinimg.com/736x/cc/8c/b2/cc8cb296b8b2c9de8badd6ccc332815a.jpg);
            height: 100vh;
            width: 100vw;
            background-size: cover;
            background-position: center;
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-repeat: no-repeat;
        }
        .container {
            width: 400px;
            margin: 50px auto;
            background-color: rgba(255, 255, 255, 0.8);
            padding: 20px;
            border: 1px solid #ddd;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            
        }
        .h1 {
            font-size: 24px;
            margin-bottom: 20px;
            text-align: center;
            top: 200px;
            right: 1100px;
        }
        .label {
            font-size: 18px;
            display: block;
            margin-bottom: 8px;
            text-align: center;
        }
        .input {
            width: 100%;
            padding: 10px;
            font-size: 16px;
            margin-bottom: 20px;
            border: 1px solid #ddd;
            border-radius: 4px;
            box-sizing: border-box;
        }
        .button {
            background-color: #0896ba;
            color: #fff;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            display: block;
            margin: 0 auto;
        }
        .button:hover {
            background-color: #4e9bc4;
        }
        .result {
            margin-top: 80px;
            font-size: 20px;
            padding: 100px;
            background-color: #3e7e8e;
            border: 1px solid #d4f4d4;
            border-radius: 4px;
            display: none;
            text-align: center;
            top: 200px;
            right: 1100px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1 class="h1">Incandescent Bulb Power Calculator</h1>
        <form id="calculatorForm">
            <label for="intensity" class="label">Enter Intensity (I in Amperes):</label>
            <input type="number" id="intensity" name="intensity" step="any" required class="input">
            <label for="resistance" class="label">Enter Resistance (R in Ohms):</label>
            <input type="number" id="resistance" name="resistance" step="any" required class="input">
            <button type="button" onclick="calculatePower()" class="button">Calculate Power</button>
        </form>
        <div class="result" id="result">Power (P) = <span id="powerResult"></span> Watts</div>
    </div>

    <script>
        function calculatePower() {
            const intensity = parseFloat(document.getElementById("intensity").value);
            const resistance = parseFloat(document.getElementById("resistance").value);
            if (isNaN(intensity) || isNaN(resistance) || intensity <= 0 || resistance <= 0) {
                alert("Please enter valid positive numbers for Intensity and Resistance.");
                return;
            }
            const power = Math.pow(intensity, 2) * resistance;
            document.getElementById("powerResult").innerText = power.toFixed(2);
            document.getElementById("result").style.display = "block";
        }
    </script>
</body>
</html>

```
# SERVER SIDE PROCESSING:
![Screenshot 2024-12-14 175347](https://github.com/user-attachments/assets/2e1b8a72-f41d-4e43-8299-b73e40fe755b)
# HOMEPAGE:
![Screenshot 2024-12-14 175419](https://github.com/user-attachments/assets/dc3c2bb7-f245-4c1e-b71e-3a7bc48b188d)
# RESULT:
The program for performing server side processing is completed successfully.
