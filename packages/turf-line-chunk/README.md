# turf-line-chunk

# lineChunk

Divides a [LineString](http://geojson.org/geojson-spec.html#linestring) into chunks of a specified length.
If the line is shorter than the segment length then the original line is returned.

**Parameters**

-   `featureIn` **([FeatureCollection](http://geojson.org/geojson-spec.html#feature-collection-objects) \| [Feature](http://geojson.org/geojson-spec.html#feature-objects)&lt;([LineString](http://geojson.org/geojson-spec.html#linestring) \| [MultiLineString](http://geojson.org/geojson-spec.html#multilinestring))>)** the lines to split
-   `segmentLength` **[number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)** how long to make each segment
-   `units` **\[[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)]** units can be degrees, radians, miles, or kilometers (optional, default `'kilometers'`)
-   `reverse` **\[[boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean)]** reverses coordinates to start the first chunked segment at the end (optional, default `false`)

**Examples**

```javascript
var line = {
  "type": "Feature",
  "properties": {},
  "geometry": {
    "type": "LineString",
    "coordinates": [
      [-95, 40],
      [-93, 45],
      [-85, 50]
    ]
  }
};
var result = turf.lineChunk(line, 15, 'miles');
//=result
```

Returns **[FeatureCollection](http://geojson.org/geojson-spec.html#feature-collection-objects)&lt;[LineString](http://geojson.org/geojson-spec.html#linestring)>** collection of line segments

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
$ npm install turf-line-chunk
```

Or install the Turf module that includes it as a function:

```sh
$ npm install @turf/turf
```
