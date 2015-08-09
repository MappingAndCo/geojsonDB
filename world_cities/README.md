# geojsonDB

Original shape file ```ne_110m_populated_places``` v2.0.0 from   [naturalearthdata.com](http://www.naturalearthdata.com) 

Link:

http://www.naturalearthdata.com/download/110m/cultural/ne_110m_populated_places.zip

Just use a link like this:

http://mappingandco.github.io/geojsonDB/word_countries/countries.json


Example of how to add countries geojson to a leaflet map:

```
var geojsonURL = "http://mappingandco.github.io/geojsonDB/world_cities/countries.json"
$.getJSON(geojsonURL, function(response) {
    var geojsonLayer = new L.GeoJSON(response, {
        style: style,
        onEachFeature: onEachFeature
    });
    geojsonLayer.addTo(map);    
});