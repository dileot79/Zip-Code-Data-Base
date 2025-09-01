<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>ZIP Code Search - Amazing Demolition of NJ</title>
  <style>
    body { font-family: Arial, sans-serif; background: #f9f9f9; margin: 40px; color: #333; }
    .container { max-width: 500px; margin: auto; padding: 20px; background: #fff; border-radius: 10px; box-shadow: 0 2px 10px rgba(0,0,0,0.1); }
    h2 { text-align: center; }
    input { width: 100%; padding: 10px; margin: 10px 0; border-radius: 5px; border: 1px solid #ccc; }
    button { padding: 10px 15px; background: #007BFF; border: none; border-radius: 5px; color: white; cursor: pointer; width: 100%; }
    button:hover { background: #0056b3; }
    .result { margin-top: 20px; padding: 15px; background: #f1f1f1; border-radius: 8px; }
    ul { margin: 10px 0 0 20px; }
  </style>
</head>
<body>
  <div class="container">
    <h2>Find Services in Your Area</h2>
    <input type="text" id="zipInput" placeholder="Enter ZIP Code">
    <button onclick="searchZip()">Search</button>
    <div class="result" id="result"></div>
  </div>

  <script>
    // Sample ZIP → City/State mapping
    const zipDatabase = {
      "07001": { city: "Avenel", state: "NJ" },
      "07002": { city: "Bayonne", state: "NJ" },
      "10001": { city: "New York", state: "NY" },
      "60601": { city: "Chicago", state: "IL" },
      "94102": { city: "San Francisco", state: "CA" }
    };

    // Products per state
    const stateProducts = {
      "NJ": ["10-Yard Dumpster", "20-Yard Dumpster", "Concrete Removal"],
      "NY": ["Interior Demolition", "Exterior Demolition", "Roll-off Dumpster"],
      "IL": ["Garage Demolition", "House Demolition", "Construction Debris Removal"],
      "CA": ["Commercial Demo", "Residential Demo", "Dumpster Rentals"]
    };

    function searchZip() {
      const zip = document.getElementById("zipInput").value.trim();
      const resultDiv = document.getElementById("result");

      if (zipDatabase[zip]) {
        const { city, state } = zipDatabase[zip];
        const products = stateProducts[state] || ["Products not available for this state"];
        resultDiv.innerHTML = `
          <h3>Results for ZIP: ${zip}</h3>
          <p><strong>City:</strong> ${city}</p>
          <p><strong>State:</strong> ${state}</p>
          <p><strong>Products we offer in this area:</strong></p>
          <ul>
            ${products.map(p => `<li>${p}</li>`).join("")}
          </ul>
        `;
      } else {
        resultDiv.innerHTML = `<p style="color:red;">Sorry, no data available for ZIP ${zip}.</p>`;
      }
    }
  </script>
</body>
</html>
