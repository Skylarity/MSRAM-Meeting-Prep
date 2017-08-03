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

D3 also shines when you're just using its data manipulation methods. The second use case uses D3 to filter data and map it to sizes/colors/other data/etc. and then we use these values to display data via HTML5 canvas.

## Canvas

Added in [HTML5](https://developer.mozilla.org/en-US/docs/HTML/HTML5), the HTML `<canvas>` element can be used to draw graphics via scripting in JavaScript. For example, it can be used to draw graphs, make photo compositions, create animations, or even do real-time video processing or rendering. <sup>[[source](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API)]</sup>

### Advantages

We prefer canvas over SVG for performance and flexibility reasons. SVGs live in the DOM, which adds memory and rendering overhead, whereas canvas graphics exist for as long as it takes to draw the image onto the canvas. Canvas graphics may also be animated and otherwise process in ways that SVGs cannot.

### Disadvantages

User interaction with the HTML5 canvas is more difficult than interaction with DOM-based approaches like SVG. Since there are no elements to attach listeners to, you must track the mouse position and perform calculations to see if it is within the area you want to be clickable.

### Ideal Use Cases

## Three.js

[Three.js](https://threejs.org/) is a 2D and 3D graphics library written for WebGL and canvas.

### Advantages

### Disadvantages

### Ideal Use Cases

## Our Recommendation

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

## Our Recommendation

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

## Our Recommendation
