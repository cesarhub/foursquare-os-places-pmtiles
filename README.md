# foursquare-os-places-pmtiles
All 100M+ open source places of Foursquare in a single PMTiles file

Read the [Foursquare blog post...](https://location.foursquare.com/resources/blog/products/foursquare-open-source-places-a-new-foundational-dataset-for-the-geospatial-community/)


## Demo

https://wipfli.github.io/foursquare-os-places-pmtiles

<a href="https://wipfli.github.io/foursquare-os-places-pmtiles">
<img src="screenshot.png">
</a>

## Download

[foursquare-os-places-2024-11-20.pmtiles](https://oliverwipfli.ch/data/foursquare-os-places-2024-11-20.pmtiles) (22 GB)
note to self, I've also downloaded the file locally when forking this

## Steps

Install DuckDB and Tippecanoe.

Run `./run.sh`. This calls duckdb and gets all the rows, structures them into geojson, and feeds them to Tippecanoe.

## Acknowledgements

Inspired by @bdon's [Overture places script](https://github.com/OvertureMaps/overture-tiles/blob/main/scripts/2024-04-16-beta/places.sh). Uses @msbarry's [Overture html viewer](https://github.com/msbarry/planetiler-overture-demo/blob/main/index.html).

## Extract GeoJSON for a Bounding Box

[`rapperswil-geojson.sh`](rapperswil-geojson.sh) is an example how to extract data with DuckDB for a given bounding box, here for the town [Rapperswil](https://wipfli.github.io/foursquare-os-places-pmtiles/#map=14/47.22803/8.82657/0/2) in Switzerland. It uses a `WHERE latitude BETWEEN minLat AND maxLat`...
