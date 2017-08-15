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

Added in [HTML5](https://developer.mozilla.org/en-US/docs/HTML/HTML5), the HTML `<canvas>` element can be used to draw graphics via scripting in JavaScript. <sup>[[source](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API)]</sup>

### Advantages

Canvas is preferred over SVG when performance and flexibility are desired. SVGs live in the DOM, which adds memory and rendering overhead, whereas canvas graphics exist for as long as it takes to draw the image onto the canvas. Canvas graphics may also be animated and otherwise processed in ways that SVGs cannot.

Canvas also provides us the ability to post-process raster images and videos on the fly. This allows us to perform interesting techniques on data that has either been pre-rendered or rendered offscreen.

### Disadvantages

User interaction with the HTML5 canvas is more difficult than interaction with DOM-based approaches like SVG. Since there are no elements to attach listeners to, you must track the mouse position and perform calculations to see if it is within the area you want to be clickable.

### Ideal Use Cases

## Three.js

[Three.js](https://threejs.org/) is a 2D and 3D graphics library written for WebGL and canvas.

### Advantages

Three.js allows us to easily render visualizations in 3D.

### Disadvantages

The overhead of rendering a full-3D scene in a web browser is too much for some client machines to handle, and limits us to only machines with adequate hardware.

### Ideal Use Cases

Showcasing data in a stylized and three-dimensional manner.

![threejs-demo](images/threejs-demo.gif)

[[source](http://armsglobe.chromeexperiments.com/)]

# Mapping Technologies

## Leaflet.js

[Leaflet.js](http://leafletjs.com/) is a mapping library that allows us to display map tiles and data together easily.

### Advantages

Leaflet is very simple and extensible. Using it in a project requires minimal setup and execution.

Leaflet can render data in both SVG and HTML5 canvas, and provides an API for using the same code to generate either.

### Disadvantages

Leaflet by itself just provides the framework to display map tiles, data, and other things. If you want a basemap you must use tiles from a third-party source such as [Mapbox](#mapbox).

### Ideal Use Cases

Leaflet has two primary functions for us:

1. Displaying basemap tiles
1. Displaying polygonal data on the map (in most cases)

We then use [D3.js](#d3js), [Turf.js](#turfjs), and/or [Three.js](#threejs) to augment and extend the existing data.

![leaflet-demo](images/leaflet-demo.png)

## Mapbox

[Mapbox](https://www.mapbox.com/) is a JavaScript library built on [Leaflet.js](#leafletjs). It provides additional functionality for data-driving the styles of data displayed on the map, as well a suite of tools dedicated to creating and editing map tile styles.

### Advantages

Mapbox has two implementations, a raster-based system, and a WebGL based vector system.

MapboxGL provides 3D rendering capabilities as well as a performance boost and seamless transitions between zoom level (no need to lead new raster tiles when you're just loading one set of vector tiles).

Mapbox's map style creation tool is fantastic for both prototyping in and implementing final designs.

### Disadvantages

Mapbox only really has one major disadvantage if you're choosing between it and Leaflet.js. This is that you cannot plug D3.js' data manipulation methods easily into Mapbox's proprietary data-driven styling methods.

Also, a recent version of Internet Explorer 11 introduced a bug when adding data sources to a Mapbox map, causing a blank screen. This is obviously not an issue when IE11 is not required for the project.

### Ideal Use Cases

Mapbox can be used interchangeably with Leaflet.js for projects that do not require IE11 support.

In cases where three-dimensional representation may help the visual cognition of data, Mapbox is incredibly easy to use.

![mapbox-demo](images/mapbox-demo.png)

Mapbox's data-driven styling methods also simplify data visualization, if the project scope fits within the limitations of said methods.

## Turf.js

[Turf.js](http://turfjs.org/) is an extremely powerful geospatial vector analysis library.

### Advantages

Turf.js reduces complex geographical operations down to a simple method call.

### Disadvantages

Turf.js must be used client-side if you are not using Node.js as your backend. This means that complex calculations may potentially be offloaded to the client machine.

## ESRI/ArcGIS JavaScript API

`TODO`

### Advantages

`TODO`

- Compatibility with ESRI

### Disadvantages

`TODO`

- Flexibility

### Ideal Use Cases

Turf.js is ideal for optimizing user-interaction with data - i.e. detecting if geographical points are within a selection, creating grids or random areas of arbitrary data, scaling, rotating, or otherwise transforming data, etc.

Here, Turf.js is used to find the nearest hospital to a branch of a public library selected by the user. <sup>[[source](https://bl.ocks.org/pdbartsch/44332447869f2a450144)]</sup>

![turf-demo](images/turf-demo.png)

# User Interface Framework Technology

## Angular.js v1.x

Angular 1 is a framework for single-page-app management and control. It provides functionality for creating reusable components and data sharing.

### Advantages

Angular is a large framework, and as such has many built-in pieces of functionality that can be applied to many use-cases and design practices.

Angular's "opinionated" nature can be advantageous once you learn the design practices, because it can allow you to code large projects with much less overhead. <sup>[[opinionation](https://stackoverflow.com/a/802064/2651657)]</sup>

### Disadvantages

Angular 1.x is nearing its end-of-life. It also has a rather large footprint, and is slower than its competitors.

Angular's "opinionated" nature can be limiting if you are trying to do something in a way that the developers did not account for. <sup>[[opinionation](https://stackoverflow.com/a/802064/2651657)]</sup>

### Ideal Use Cases

Angular 1 should be used in a scenario where you need lots of support. There is a large ecosystem of people who either have used or are currently using Angular 1, and there are a huge number of help threads and libraries.

## Angular v2+

Angular 2 (and above) is the rewrite of Angular 1, focused on simplifying and optimizing the framework.

### Advantages

Angular 2+ is simpler to write than Angular 1, and the recommended language to write it in is TypeScript. Angular 2+ provides all of the functionality of Angular 1, but the framework is generally smaller, easier to write and comprehend, and faster.

### Disadvantages

Angular 2+ still has the "opinionated" nature of Angular 1, and forces you down its development paradigm. Angular 2+ may perform faster than Angular 1, but it is still slower than React or Vue.

### Ideal Use Cases

Angular 2+ is optimal for a scenario in which you prefer a framework with a heavy structure, and provides a specific way to accomplish tasks. This can be good when you are working in a situation where you want no wiggle room, i.e. many developers are working on a project, and organization is imperative.

## React.js

React a is a library (not a framework) that provides an interface for managing UI components. It is entirely flexible, and can fit within whatever framework or paradigm you are using.

### Advantages

React is very fast, utilizing a Virtual DOM to avoid unnecessary UI repaints (like Vue). Since React is just a UI library, and not an entire framework, it can be used in many ways, and not interfere with your model or control systems.

### Disadvantages

An artifact of being just a UI library, React forces the user to either use other libraries or write custom code in order to run the other parts of their application. While there are fantastic libraries out there, sometimes the design paradigms inherent in an "opinionated" framework can be very helpful for writing and prototyping extremely quickly.

### Ideal Use Cases

React is ideal when you need a flexible, free-form UI that can fit around whatever application paradigm you prefer.

## Vue.js

[Vue.js](https://vuejs.org/) is a progressive framework for building user interfaces. Unlike other monolithic frameworks, Vue is designed from the ground up to be incrementally adoptable. The core library is focused on the view layer only, and is very easy to pick up and integrate with other libraries or existing projects. On the other hand, Vue is also perfectly capable of powering sophisticated Single-Page Applications when used in combination with [modern tooling](https://vuejs.org/v2/guide/single-file-components.html) <sup>(`.vue` files, detailed [below](#advantages-9))</sup> and [supporting libraries](https://github.com/vuejs/awesome-vue#components--libraries). <sup>[[source](https://vuejs.org/v2/guide/)]</sup>

[Vue Benchmark](https://vuejs.org/v2/guide/comparison.html)

### Advantages

Of the three frameworks we're reviewing, Vue.js has the smallest footprint and the fastest benchmarks. Leveraging the power of the virtual DOM, it avoids any UI repaints until necessary. Vue's architecture also allows for more performant JS operations to achieve the same results.

Vue's "opinionated" nature can be advantageous once you learn its design practices, because it can allow you to code large projects with much less development overhead. <sup>[[opinionation](https://stackoverflow.com/a/802064/2651657)]</sup>

Vue allows you to write all of your code (HTML, JS, and CSS) inside one file - a `.vue` file. This allows segregation of code and simplification of organization. Vue accomplishes this with [Webpack](https://webpack.js.org/). Each `.vue` file consists of a `<template>`, `<script>`, and `<style>` tag, which you write your HTML, JS, and CSS in respectively. Each tag also takes a `lang` attribute, where you can specify a pre or post processor for the language you are writing. For instance, you can put `lang="scss"` on your `<style>` tag, write in SCSS, and Webpack will auto-compile to CSS.

In a best of both worlds kind of way, Vue is developed similarly to Angular, but performs similarly to React.

### Disadvantages

Vue.js version 2, having been only fairly recently released, has less community support than React or Angular.

Both a blessing and a curse, Vue's semi-"opinionated" nature can be restrictive in certain cases, rather than helpful.

### Ideal Use Cases

Vue is ideally used for anything where you need high performance, and prefer a framework that provides some structure.
