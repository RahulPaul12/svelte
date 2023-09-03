<script>
  import { onMount } from 'svelte';
  import { Map, View } from 'ol';
  import GeoJSON from 'ol/format/GeoJSON';
  import { Tile as TileLayer, Vector as VectorLayer } from 'ol/layer';
  import { OSM, Vector as VectorSource } from 'ol/source';
  import { Style, Fill } from 'ol/style';

  let map;

  onMount(() => {
    // Create a map and set its target div to the map container
    map = new Map({
      target: 'map-container',
      layers: [
        new TileLayer({
          source: new OSM()
        })
      ],
      view: new View({
        center: [0, 0],
        zoom: 2
      })
    });

    // Add GeoJSON data to the map
    const vectorSource = new VectorSource({
      format: new GeoJSON(),
      url: '/countries.geojson' // Adjust the path based on your project structure
    });

    const vectorLayer = new VectorLayer({
      source: vectorSource,
      style: new Style({
        fill: new Fill({
          color: 'rgb(0,106,78, 0.75)' // Set the fill color to red
        })
      })
    });

    map.addLayer(vectorLayer);
  });
</script>

<style>
  #map-container {
    width: 100%;
    height: 100vh; /* Adjust the height as needed */
  }
</style>

<div id="map-container"></div>
