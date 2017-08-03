# Visualization Technologies

## D3.js

[D3.js](https://d3js.org/) is a JavaScript library for manipulating documents based on data. <sup>[[source](https://d3js.org/)]</sup>

D3 allows the user to dynamically create and update content in a web browser by looping through a data set (or multiple) and applying data-driven styles and transformations to either DOM elements or an [HTML5 canvas](#canvas).

### Advantages

### Disadvantages

### Ideal Use Cases

## Canvas

Added in [HTML5](https://developer.mozilla.org/en-US/docs/HTML/HTML5), the HTML `<canvas>` element can be used to draw graphics via scripting in JavaScript. For example, it can be used to draw graphs, make photo compositions, create animations, or even do real-time video processing or rendering. <sup>[[source](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API)]</sup>

We prefer canvas over SVG for performance and flexibility reasons. SVGs live in the DOM, which adds memory and rendering overhead, whereas canvas graphics exist for as long as it takes to draw the image onto the canvas. Canvas graphics may also be animated and otherwise process in ways that SVGs cannot.

### Advantages

### Disadvantages

### Ideal Use Cases

## Three.js

[Three.js](https://threejs.org/) is a 2D and 3D graphics library written for WebGL and canvas.

### Advantages

### Disadvantages

### Ideal Use Cases

## Our Recomendation

# Mapping Technologies

## Leaflet.js

[Leaflet.js](http://leafletjs.com/) is a mapping library that allows us to display map tiles and data together easily.

Leaflet has two primary functions for us:

1. Displaying basemap tiles
1. Displaying polygonal data on the map (in most cases)

We then use [D3.js](#d3js), [Turf.js](#turfjs), and/or [Three.js](#threejs) to augment and extend the existing data.

### Advantages

### Disadvantages

### Ideal Use Cases

## Turf.js

[Turf.js](http://turfjs.org/) is an extremely powerful geospatial vector analysis library.

### Advantages

### Disadvantages

### Ideal Use Cases

## Our Recomendation

# User Interface Framework Technology

## Angular.js

Description here

### Advantages

### Disadvantages

### Ideal Use Cases

## React.js

Description here

### Advantages

### Disadvantages

### Ideal Use Cases

## Vue.js

Description here

### Advantages

`like a combo of Angular and React`

### Disadvantages

### Ideal Use Cases

## Our Recomendation
