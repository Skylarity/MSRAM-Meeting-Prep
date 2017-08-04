# Visualization Technologies

## D3.js

[D3.js](https://d3js.org/) is a JavaScript library for manipulating documents based on data. <sup>[[source](https://d3js.org/)]</sup>

### Advantages

D3 allows the user to dynamically create and update content in a web browser by looping through a data set (or multiple) and applying data-driven styles and transformations to either DOM elements or an [HTML5 canvas](#canvas).

### Disadvantages

While D3 is optimized and useful for interacting with DOM elements, only the portions that deal with data manipulation may be used when dealing with HTML5 canvas, requiring custom solutions or third-party libraries.

### Ideal Use Cases

D3 has two optimal use cases.

In the first scenario, D3 is used to both manipulate data and display it in the DOM via SVG. This is most useful for interactive graphs or data manipulation controls and filters.

![D3 used for user-controlled data filtering](images/d3-filtering.gif)

D3 also shines when you're just using its data manipulation methods. The second use case uses D3 to filter data and map it to sizes/colors/other data/etc. and then we use these values to display data via HTML5 canvas.

## Canvas

Added in [HTML5](https://developer.mozilla.org/en-US/docs/HTML/HTML5), the HTML `<canvas>` element can be used to draw graphics via scripting in JavaScript. For example, it can be used to draw graphs, make photo compositions, create animations, or even do real-time video processing or rendering. <sup>[[source](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API)]</sup>

### Advantages

Canvas is preferred over SVG when performance and flexibility are desired. SVGs live in the DOM, which adds memory and rendering overhead, whereas canvas graphics exist for as long as it takes to draw the image onto the canvas. Canvas graphics may also be animated and otherwise process in ways that SVGs cannot.

### Disadvantages

User interaction with the HTML5 canvas is more difficult than interaction with DOM-based approaches like SVG. Since there are no elements to attach listeners to, you must track the mouse position and perform calculations to see if it is within the area you want to be clickable.

### Ideal Use Cases

## Three.js

[Three.js](https://threejs.org/) is a 2D and 3D graphics library written for WebGL and canvas.

### Advantages

`TODO`

Three.js allows us to render visualizations in 3D.

### Disadvantages

Performance. `TODO: EXPAND`

### Ideal Use Cases

Showcasing data in a stylized and three-dimensional manner.

`TODO: ![three-js-demo](images\three-js-demo.gif)`

[[source](https://paperplanes.world/)]

## Our Recommendation

`TODO`

- D3 + SVG for some things
- D3 + HTML5 canvas or Three.js for things that require performance or extensibility

# Mapping Technologies

## Leaflet.js

[Leaflet.js](http://leafletjs.com/) is a mapping library that allows us to display map tiles and data together easily.

Leaflet has two primary functions for us:

1. Displaying basemap tiles
1. Displaying polygonal data on the map (in most cases)

We then use [D3.js](#d3js), [Turf.js](#turfjs), and/or [Three.js](#threejs) to augment and extend the existing data.

### Advantages

`TODO`

### Disadvantages

`TODO`

### Ideal Use Cases

`TODO`

## Mapbox

[Mapbox](https://www.mapbox.com/) is a JavaScript library built on [Leaflet.js](#leafletjs). It provides additional functionality for data-driving the styles of data displayed on the map, as well a suite of tools dedicated to creating and editing map tile styles.

### Advantages

Mapbox has two implementations, a raster-based system, and a WebGL based vector system.

MapboxGL provides 3D rendering capabilities as well as a performance boost and seamless transitions between zoom level (no need to lead new raster tiles when you're just loading one set of vector tiles).

### Disadvantages

Mapbox only really has one major disadvantage if you're choosing between it and Leaflet.js. This is that you cannot plug D3.js' data manipulation methods easily into Mapbox's proprietary data-driven styling methods.

Also, a recent version of Internet Explorer 11 introduced a bug when adding data sources to a Mapbox map, causing a blank screen. This is obviously not an issue when IE11 is not required for the project.

### Ideal Use Cases

In cases where three-dimensional representation may help the visual cognition of data, Mapbox is incredibly easy to use.

![mapbox-demo](images/mapbox-demo.png)

## Turf.js

[Turf.js](http://turfjs.org/) is an extremely powerful geospatial vector analysis library.

### Advantages

Turf.js reduces complex geographical operations down to a simple method call.

### Disadvantages

Turf.js must be used client-side if you are not using Node.js as your backend. This means that complex calculations may potentially be offloaded to the client machine.

### Ideal Use Cases

Turf.js is ideal for optimizing user-interaction with data - i.e. detecting if geographical points are within a selection, creating grids or random areas of arbitrary data, scaling, rotating, or otherwise transforming data, etc.

Here, Turf.js is used to find the nearest hospital to a branch of a public library selected by the user. <sup>[[source](https://bl.ocks.org/pdbartsch/44332447869f2a450144)]</sup>

![turf-demo](images/turf-demo.png)

## Our Recommendation

`TODO`

- Leaflet + Turf + D3 for most use cases
- Mapbox + Turf for non-IE11 cases or cases with 3D requirements

# User Interface Framework Technology

## Angular.js

`TODO`

Description here

### Advantages

`TODO`

### Disadvantages

`TODO`

### Ideal Use Cases

`TODO`

## React.js

`TODO`

Description here

### Advantages

`TODO`

- Extreme extensibility

### Disadvantages

`TODO`

### Ideal Use Cases

`TODO`

## Vue.js

`TODO`

Description here

### Advantages

`TODO`

- Like a combo of Angular and React

### Disadvantages

`TODO`

### Ideal Use Cases

`TODO`

## Our Recommendation

`TODO`
