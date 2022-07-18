# OpenLayers

[OpenLayers](https://openlayers.org/) is a high-performance, feature-packed library for creating interactive maps on the web. It can display map tiles, vector data and markers loaded from any source on any web page. OpenLayers has been developed to further the use of geographic information of all kinds. It is completely free, Open Source JavaScript, released under the [BSD 2-Clause License](https://opensource.org/licenses/BSD-2-Clause).

## Getting Started

Install the [`ol` package](https://www.npmjs.com/package/ol):

```
npm install ol
```

Import just what you need for your application:

```js
import Map from 'ol/Map';
import View from 'ol/View';
import TileLayer from 'ol/layer/Tile';
import XYZ from 'ol/source/XYZ';

new Map({
  target: 'map',
  layers: [
    new TileLayer({
      source: new XYZ({
        url: 'https://{a-c}.tile.openstreetmap.org/{z}/{x}/{y}.png'
      })
    })
  ],
  view: new View({
    center: [0, 0],
    zoom: 2
  })
});
```

See the following examples for more detail on bundling OpenLayers with your application:

 * Using [Vite](https://github.com/openlayers/ol-vite)
 * Using [Rollup](https://github.com/openlayers/ol-rollup)
 * Using [webpack](https://github.com/openlayers/ol-webpack)
 * Using [Parcel](https://github.com/openlayers/ol-parcel)



See our [GitHub sponsors page](https://github.com/sponsors/openlayers) or [Open Collective](https://opencollective.com/openlayers/contribute/sponsors-214/checkout) if you too are interested in becoming a regular sponsor.





{
  "name": "webgis",
  "version": "1.0.0",
  "description": "웹기반서비스 구현하기 (공간정보서비스 개발)",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "start": "parcel index.html",
    "build": "parcel build --public-url . index.html"
  },
  "repository": {
    "type": "git",
    "url": "git+https://github.com/locking92/webgis.git"
  },
  "author": "",
  "license": "ISC",
  "bugs": {
    "url": "https://github.com/locking92/webgis/issues"
  },
  "homepage": "https://github.com/locking92/webgis#readme",
  "dependencies": {
    "ol": "^6.14.1"
  },
  "devDependencies": {
    "parcel-bundler": "^1.12.5"
  }
}
