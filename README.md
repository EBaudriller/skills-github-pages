<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <title>Carte Interactive</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <!-- Leaflet CSS -->
  <link rel="stylesheet" href="https://unpkg.com/leaflet/dist/leaflet.css" />
  <style>
    #map {
      height: 400px;
      width: 80%;
      max-width: 600px;
      margin: auto;
      border: 2px solid #4CAF50;
      border-radius: 10px;
    }
  </style>
</head>
<body>

  <h2 style="text-align:center;">Petite carte interactive</h2>
  <div id="map"></div>

  <!-- Leaflet JS -->
  <script src="https://unpkg.com/leaflet/dist/leaflet.js"></script>
  <script>
    var map = L.map('map').setView([43.7, 7.2], 10);

    L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
      attribution: '&copy; OpenStreetMap contributors'
    }).addTo(map);

    L.marker([43.7, 7.2]).addTo(map)
      .bindPopup('PNR Préalpes d\'Azur')
      .openPopup();
  </script>

</body>
</html>
