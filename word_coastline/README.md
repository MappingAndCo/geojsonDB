# geojsonDB word coastline



Just use a link like this:

http://mappingandco.github.io/geojsonDB/word_coastline/ne_10m_coastline.geojson


Example of how to add countries geojson to a leaflet map:

```
var countriesGeojsonURL = "http://mappingandco.github.io/geojsonDB/word_coastline/ne_10m_coastline.geojson"
$.getJSON(countriesGeojsonURL, function(response) {
    var geojsonLayer = new L.GeoJSON(response, {
	    style: style,
	    onEachFeature: onEachFeature
	});
    geojsonLayer.addTo(map);    
});
```

### Data source

About

Ocean coastline, including major islands. Coastline is matched to land and water polygons. The Caspian Sea, which is technically a lake, is included. The ocean coastline, the foundation for building all of NEV, primarily derives from World Data Bank 2 with modest generalization applied via line simplification in Adobe Illustrator. The Antarctica coast derives from NASA Mosaic of Antarctica.

version 3.0.0

http://www.naturalearthdata.com/downloads/10m-physical-vectors/

Natural earth data terms of use:

http://www.naturalearthdata.com/about/terms-of-use/