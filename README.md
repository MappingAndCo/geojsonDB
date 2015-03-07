# geojsonDB


This repo include geojson files that can be used anywhere

<blockquote class="twitter-tweet" lang="es"><p>Good news if you use GitHub to store GeoJSON: All GitHub Pages sites now have CORS headers set by default so you can use the data anywhere.</p>&mdash; Ben Balter (@BenBalter) <a href="https://twitter.com/BenBalter/status/573941108247519232">marzo 6, 2015</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

Just use a link like this:

http://mappingandco.github.io/geojsonDB/word_countries/countries.json


Example of how to add countries geojson to a leaflet map:

```
var countriesGeojsonURL = "http://mappingandco.github.io/geojsonDB/word_countries/countries.json"
$.getJSON(countriesGeojsonURL, function(response) {
    var geojsonLayer = new L.GeoJSON(response, {
	    style: style,
	    onEachFeature: onEachFeature
	});
    geojsonLayer.addTo(map);    
});
```