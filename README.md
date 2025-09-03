<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Bike Rental Service</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f5f5f5;
      margin: 0;
      padding: 20px;
    }
    .container {
      max-width: 500px;
      margin: auto;
      background: #fff;
      padding: 20px;
      border-radius: 12px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
    }
    h2 {
      text-align: center;
      color: #333;
    }
    label {
      display: block;
      margin-top: 10px;
      font-weight: bold;
    }
    select, input {
      width: 100%;
      padding: 8px;
      margin-top: 5px;
      border-radius: 6px;
      border: 1px solid #ccc;
    }
    button {
      margin-top: 15px;
      width: 100%;
      padding: 10px;
      background: #28a745;
      color: white;
      border: none;
      border-radius: 8px;
      font-size: 16px;
      cursor: pointer;
    }
    button:hover {
      background: #218838;
    }
    .result {
      margin-top: 20px;
      padding: 10px;
      background: #e9ffe9;
      border: 1px solid #b2dfb2;
      border-radius: 8px;
      font-weight: bold;
    }
  </style>
</head>
<body>

  <div class="container">
    <h2>🚴 Bike Rental Service</h2>
    
    <label for="bike">Choose a bike:</label>
    <select id="bike">
      <option value="100">Standard Bike - ₹100/hr</option>
      <option value="200">Mountain Bike - ₹200/hr</option>
      <option value="300">Electric Bike - ₹300/hr</option>
    </select>
    
    <label for="hours">Rental Duration (hours):</label>
    <input type="number" id="hours" min="1" value="1">
    
    <button onclick="calculateRent()">Calculate Rent</button>
    
    <div class="result" id="result">Your total will appear here.</div>
  </div>

  <script>
    function calculateRent() {
      let bikeRate = document.getElementById("bike").value;
      let hours = document.getElementById("hours").value;
      let total = bikeRate * hours;
      document.getElementById("result").innerText = "✅ Total Rent: ₹" + total;
    }
  </script>

</body>
</html>
