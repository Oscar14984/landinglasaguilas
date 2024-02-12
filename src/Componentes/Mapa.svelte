<script>
    import { onMount } from 'svelte';
    import L from 'leaflet';
  
    let map;
  
    onMount(() => {
      map = L.map('map').setView([19.357028, -99.1985], 13);
      L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
        attribution: '© OpenStreetMap contributors',
      }).addTo(map);
  
      
      const divIcon = L.divIcon({
        html: '<div><YourSvelteComponent /></div>', 
        className: 'custom-icon-class', 
      });
  
      
      L.marker([19.357028, -99.1985], { icon: divIcon }).addTo(map);
    });
  </script>
  
  <style>
   
  </style>
  
  <div id="map"></div>