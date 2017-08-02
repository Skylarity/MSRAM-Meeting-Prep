# D3.js

[D3.js](https://d3js.org/) is a JavaScript library for manipulating documents based on data. <sup>[[source](https://d3js.org/)]</sup>

D3 allows the user to dynamically create and update content in a web browser by looping through a data set (or multiple) and applying data-driven styles and transformations to either DOM elements or an [HTML5 canvas](#canvas).

# Canvas

Added in [HTML5](https://developer.mozilla.org/en-US/docs/HTML/HTML5), the HTML <canvas> element can be used to draw graphics via scripting in JavaScript. For example, it can be used to draw graphs, make photo compositions, create animations, or even do real-time video processing or rendering. <sup>[[source](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API)]</sup>

We prefer canvas over SVG for performance and flexibility reasons. SVGs live in the DOM, which adds memory and rendering overhead, whereas canvas elements exist for as long as it takes to draw the image onto the canvas. Canvas elements may also be animated and otherwise process in ways that SVGs cannot.

# Leaflet.js

[Leaflet.js](http://leafletjs.com/) is a mapping library that allows us to display map tiles and data together easily.

Leaflet has two primary functions for us:

1. Displaying basemap tiles
1. Displaying polygonal data on the map (in most cases)

We then use [D3.js](#d3js), [Turf.js](#turfjs), and/or [Three.js](#three.js) to augment and extend the existing data.

# Turf.js

[Turf.js](http://turfjs.org/) is an extremely powerful geospatial analysis library.

# Three.js

**TODO**

[Three.js](https://threejs.org/) is a 2D and 3D graphics library written for WebGL and canvas.