---
draft: false
title: "Il nostro Viaggio di Nozze"
---

## 🌎❤️ Destinazione: Argentina

"Una terra lontana… dove la natura regna sovrana, i paesaggi cambiano ad ogni curva e ogni giorno è una nuova avventura."

<br>

<!-- MapLibre CSS & JS -->
<link href="https://unpkg.com/maplibre-gl@2.4.0/dist/maplibre-gl.css" rel="stylesheet" />
<script src="https://unpkg.com/maplibre-gl@2.4.0/dist/maplibre-gl.js"></script>

<style>
/* Rimuove sfondo bianco di default dal contenitore popup */
.maplibregl-popup-content {
  background: transparent !important;
  box-shadow: none !important;
  padding: 0 !important;
  border-radius: 0 !important;
}

.custom-popup {
  font-family: 'Playfair Display', serif;
  padding: 10px;
  background-color: #faf2da;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0,0,0,0.2);
  text-align: center;
  color: #4a503d;
}

.custom-popup h4 {
  margin: 0;
  font-size: 1rem;
  font-weight: 600;
}

.custom-popup a {
  display: inline-block;
  margin-top: 0.5em;
  font-size: 0.9rem;
  text-decoration: none;
  color: #8e9775;
}

.custom-popup a:hover {
  text-decoration: underline;
}
</style>

<!-- Mappa -->
<div id="map" style="height: 500px; border-radius: 10px; margin-bottom: 2rem;"></div>

<script>
  const map = new maplibregl.Map({
    container: 'map',
    style: 'https://api.maptiler.com/maps/aquarelle/style.json?key=ieAH8MPmB1ALRkjlPFmn',
    center: [-63.6167, -38.4161], // Centro Argentina
    zoom: 1.5
  });

  // Add zoom and rotation controls to the map
  map.addControl(new maplibregl.NavigationControl());

  // Coordinate list with names and anchor targets
  const places = [
    { name: "Patagonia", coords: [-68.91, -41.81], anchor: "#patagonia" },
    { name: "Perito Moreno", coords: [-73.14, -50.50], anchor: "#perito-moreno" },
    { name: "Iguazú", coords: [-54.44, -25.69], anchor: "#iguazu-falls" },
    { name: "Tilcara", coords: [-65.39, -23.58], anchor: "#tilcara" },
    { name: "Salinas Grandes", coords: [-66.03, -23.71], anchor: "#salinas-grandes" },
    { name: "Ruta 68", coords: [-65.56, -25.44], anchor: "#ruta-68" },
    { name: "Cafayate", coords: [-65.98, -26.07], anchor: "#cafayate" },
    { name: "Mendoza", coords: [-68.85, -32.89], anchor: "#mendoza" }
  ];

  map.on('load', function () {
    places.forEach((p, index) => {
      // Create a custom HTML marker
      const el = document.createElement('div');
      el.className = 'marker';
      el.style.width = '20px';
      el.style.height = '20px';
      el.style.backgroundColor = '#c0392b';
      el.style.borderRadius = '50%';
      el.style.cursor = 'pointer';
      el.style.boxShadow = '0 0 5px rgba(0,0,0,0.5)';

      const marker = new maplibregl.Marker(el)
        .setLngLat(p.coords)
        .setPopup(
          new maplibregl.Popup({ offset: 25 }).setHTML(`
            <div class="custom-popup">
              <h4>${p.name}</h4>
              <a href="${p.anchor}">Vedi tappa</a>
            </div>
          `)
        )
        .addTo(map);
    });
  });
</script>

Grazie per aver contribuito a realizzare questo viaggio di nozze, un pensiero affettuoso, che porteremo nel cuore ad ogni tappa di questa fantastica avventura. 💌

## 🧭 Il nostro itinerario

Esploreremo una terra lontana e misteriosa, ma al tempo stesso familiare per l’anima che vive nelle sue piazze e nei suoi volti. <br><br>

Dal ghiaccio millenario della Patagonia alle foreste subtropicali di Iguazú, passando per deserti, canyon colorati e bianchi salares: sarà un viaggio memorabile, a stretto contatto con la natura: **avventuroso e  indimenticabile** 🌿🏞️

## 💞 Seguici in questa avventura

Ogni tappa sarà per noi un momento speciale da ricordare. Non vediamo l’ora di partire, e condividere con voi qualche aggiornamento, lungo la strada! 📸