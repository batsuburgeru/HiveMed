<template>
<div id="pharmacySection" class="pharmacy-section">
    <div><h2>Pharmacy</h2></div>
    <div class="flex">
        <div class="btn-container"><button class="locate-btn">Locate Nearest Pharmacy</button></div>
    <div class="map-container"><div id="map"></div></div>
    </div>
</div>
</template>

<script>
import { onMounted } from 'vue';
import L from 'leaflet';

export default {
  name: 'MapView',

  setup() {
    onMounted(() => {
      const mapView = L.map('map').setView([14.5953, 120.9880], 15);

      L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
        attribution: '&copy; <a href="https://www.openstreetmap.org/">OpenStreetMap</a> contributors',
        maxZoom: 18,
      }).addTo(mapView);

      L.marker([14.5953, 120.9880]).addTo(mapView)
        .bindPopup('TIP Manila')
        .openPopup();
    });

    return {};
  },
};
</script>

<style scoped>
* {
    padding: 0;
    margin: 0;
    box-sizing: border-box;
}
.pharmacy-section h2 {
    padding: 2rem 0;
    font-weight: bolder;
    font-size: 2rem;
}
.pharmacy-section {
    height: 75vh;
    width: 100vw;
    background: linear-gradient(var(--bg-color),var(--secondary-color));
    border-style:inset none none none;
}
.flex {
    display: flex;
    align-content: center;
    align-items: center;
    flex-direction: row;
    justify-content: space-between;
    padding: 1.5rem 20rem;
}
.map-container {
    border: 5px solid var(--font-color);
    height: 35rem;
    width: 35rem;
}
#map {
  height: 100%;
  width: 100%;
  z-index: 0;
}
.locate-btn {
    border-radius: 50%;
    padding: 15px 40px;
    background-color: var(--primary-color);
    border: none;
    border-radius: 50px;
    cursor: pointer;
    transition: var(--transition);
    font-weight: var(--bold-font);
    color: var(--font-color);
}
.locate-btn:hover {
    color: var(--primary-color);
    background-color: var(--secondary-bg-color);
    border-bottom: 2px solid var(--font-color);
}
</style>