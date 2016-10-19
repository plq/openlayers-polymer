# `ol-map` element

An OpenStreetMap polymer implementation. Based on OpenLayers (v3.3.0) and written in polymer 1.0 style.

## Usage

### Basic

	<ol-map longitude="{{ longitude }}" latitude="{{ latitude }}" zoom="{{ zoom }}"></ol-map>
	
<img src="https://cloud.githubusercontent.com/assets/1525818/12798245/a2f8c61e-cac8-11e5-8ad5-e8ebb0dd781d.png" width="500"/>
	
### Marker

	<ol-map latitude="53.834089" longitude="10.703718" zoom="16">
		<ol-marker longitude="10.703718" latitude="53.834089" scale="0.2" image="../data/marker-blue-shadow.png"></ol-marker>
		<ol-marker longitude="10.705318" latitude="53.835789" image="../data/marker-green-icon-shadow.png"></ol-marker>
		<ol-marker longitude="10.702318" latitude="53.832789" image="../data/marker-red.png"></ol-marker>
		<!-- marker without image attribute are displayed as circles -->
		<ol-marker longitude="10.705318" latitude="53.830789"></ol-marker>
		<ol-marker longitude="10.709318" latitude="53.839789" scale="2.5"></ol-marker>
	</ol-map>

### Polygon

    	<ol-poly fill fill-color="rgba(0,10,150,0.4)">
        	<template is="dom-repeat" items="{{ points }}">
          		<ol-point longitude$="{{ item.longitude }}" latitude$="{{ item.latitude }}"></ol-point>
        	</template>
    	</ol-poly> 

## Add `ol-map` component in your project

* Add bower dependency

  	    "dependencies": {
  		...,
    	"ol-map": "FabianBormann/ol-map"
  	    }

2.  
        
         $ bower install
	
In your project.html

	<link rel="import" href="path_to_bower_components/ol-map/ol-map.html">
	<link rel="import" href="path_to_bower_components/ol-map/ol-marker.html">
	<link rel="import" href="path_to_bower_components/ol-map/ol-point.html">
	<link rel="import" href="path_to_bower_components/ol-map/ol-poly.html">
	<link rel="import" href="path_to_bower_components/ol-map/ol-layer.html">

Now you are ready to start using the components.

## Development

Fork the repository and start to implement a new feature.
I hope to accept your pull-request if you are finished! :)

### Dependencies

Element dependencies are managed via [Bower](http://bower.io/). You can
install that via:

    npm install -g bower

Then, go ahead and download the element's dependencies:

    bower install

### Playing With ol-map

It's recommend that you use [Polyserve](https://github.com/PolymerLabs/polyserve) to keep the
bower dependencies in line. You can install it via:

    npm install -g polyserve

And you can run it via:

    polyserve

Once running, you can preview your element at `http://localhost:8080/components/ol-map/`.
