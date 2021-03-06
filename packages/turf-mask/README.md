# @turf/mask

# mask

Takes any type of [polygon](http://geojson.org/geojson-spec.html#polygon) and an optional mask and returns a [polygon](http://geojson.org/geojson-spec.html#polygon) exterior ring with holes.

**Parameters**

-   `polygon` **([FeatureCollection](http://geojson.org/geojson-spec.html#feature-collection-objects) \| [Feature](http://geojson.org/geojson-spec.html#feature-objects)&lt;([Polygon](http://geojson.org/geojson-spec.html#polygon) \| [MultiPolygon](http://geojson.org/geojson-spec.html#multipolygon))>)** GeoJSON Polygon used as interior rings or holes.
-   `mask` **\[[Feature](http://geojson.org/geojson-spec.html#feature-objects)&lt;[Polygon](http://geojson.org/geojson-spec.html#polygon)>]** GeoJSON Polygon used as the exterior ring (if undefined, the world extent is used)

**Examples**

```javascript
var poylgon = {
    "type": "Feature",
    "properties": {},
    "geometry": {
      "type": "Polygon",
      "coordinates": [
        [[100, 0], [101, 0], [101,1], [100,1], [100, 0]]
     ]
   }
}
var masked = turf.mask(polygon);
//=masked
```

Returns **[Feature](http://geojson.org/geojson-spec.html#feature-objects)&lt;[Polygon](http://geojson.org/geojson-spec.html#polygon)>** Masked Polygon (exterior ring with holes).

<!-- This file is automatically generated. Please don't edit it directly:
if you find an error, edit the source file (likely index.js), and re-run
./scripts/generate-readmes in the turf project. -->

---

This module is part of the [Turfjs project](http://turfjs.org/), an open source
module collection dedicated to geographic algorithms. It is maintained in the
[Turfjs/turf](https://github.com/Turfjs/turf) repository, where you can create
PRs and issues.

### Installation

Install this module individually:

```sh
$ npm install @turf/mask
```

Or install the Turf module that includes it as a function:

```sh
$ npm install @turf/turf
```
