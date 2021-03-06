# SharedStreets API

[![npm version](https://badge.fury.io/js/sharedstreets-api.svg)](https://badge.fury.io/js/sharedstreets-api)
[![Build Status](https://travis-ci.org/sharedstreets/sharedstreets-api.svg?branch=master)](https://travis-ci.org/sharedstreets/sharedstreets-api)

Interact directly with SharedStreet's API.

## Install

**In Node.js**

```bash
$ yarn add sharedstreets-api
```

**CommonJS**

```js
const sharedstreetsApi = require('sharedstreets-api');
```

**Typescript**

```js
import * as sharedstreetsApi from 'sharedstreets-api';
```

## In Browser

For a full list of web examples, check out [SharedStreets examples](https://github.com/sharedstreets/sharedstreets-examples).

## CLI

    Usage:
      $ sharedstreets-download-tile

    Options:
      --tile                  tile [x,y,zoom]
      --layer                 layer (geometry|intersection|metadata|reference)

    Examples:
      $ sharedstreets-download-tile --tile [1186,1466,12] --layer "geometry" > "12-1186-1466.geometry.pbf"

## API

<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

#### Table of Contents

-   [downloadTile](#downloadtile)

### downloadTile

Download Tile

**Parameters**

-   `tile` **[Array](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array)&lt;[number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number)>** Tile [x, y, z]
-   `layer` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** Layer (geometry|intersection|metadata|reference)
-   `options` **[Object](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object)** Optional parameter (optional, default `{}`)
    -   `options.output` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** Output (json|pbf) (optional, default `"pbf"`)

**Examples**

```javascript
const tile = [1186, 1466, 12];
const layer = "geometry";

sharedstreetsApi.downloadTile(tile, layer).then(data => {
  data // => PBF Buffer
})
```

Returns **[Promise](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Promise)&lt;[Buffer](https://nodejs.org/api/buffer.html)>** PBF Buffer
