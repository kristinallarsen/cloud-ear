---
title: "Tutorial: IIIF > Allmaps Editor > Leaflet Map"
excerpt_separator: "<!--more-->"
toc: true
toc_sticky: true
categories:
  - Blog
tags:
  - tutorial
  - teaching
  - maps
  - iiif
---
# How to Georeference a Map in Allmaps and Display it with Leaflet

*[Work in progress, last updated 8/17/25.]*

*A step-by-step tutorial on how to georeference a map from [DavidRumsey.com](https://www.davidrumsey.com/) or [Searchworks.Stanford.edu](https://searchworks.stanford.edu/) using [Allmaps Editor](https://editor.allmaps.org/) and then display it in a webmap made with [Leafletjs.com](https://leafletjs.com/).*

<!--more-->
## Background Info

- What is georeferencing?
[https://blogs.loc.gov/maps/2021/01/georeferencing-moving-analog-maps-into-modern-day-gis/](https://blogs.loc.gov/maps/2021/01/georeferencing-moving-analog-maps-into-modern-day-gis/) 

- What is a IIIF Manifest?
[https://iiif.io/guides/using_iiif_resources/#what-is-a-iiif-manifest](https://iiif.io/guides/using_iiif_resources/#what-is-a-iiif-manifest)

- What is Allmaps?
[https://allmaps.org/](https://allmaps.org/)

- What is Leaflet? 
[https://leafletjs.com/](https://leafletjs.com/)


## 1.  Get Started: Locate and copy a IIIF manifest link for your map

*IIIF manifest links can be found on many digital repository and library sites. Unfortunately, there’s not much standardization across sites as to where to put them in a record, so you may have to dig around for them. Below are screenshots of where to find manifest links on David Rumsey’s website and in Stanford’s Searchworks library catalog.*

***You do not need to get a link from both places, just choose one to use, copy it, and move to step 2.***

### A. Find IIIF Manifest on [Davidrumsey.com](https://www.DavidRumsey.com):

1. Click SHARE to reveal dropdown menu
2. Click “IIIF Manifests” to reveal text box with link
3. Click the “duplicate” icon to right of text box to copy link 

![Screenshot indicating locations of SHARE and IIIF Manifest links on DavidRumsey.com](https://github.com/user-attachments/assets/4776a598-9147-4e2c-ae88-5ece091f0f75)

### B. Find IIIF Manifest on Searchworks.stanford.edu:

1. Click the “hamburger menu” at upper left to reveal metadata sidebar 
2. Scroll all the way to the bottom of the sidebar
3. Locate the link below “IIIF manifest”
4. Right click to copy the link

![Screenshot indicating location of hamburger menua and IIIF manifest link on Searchworks.](https://github.com/user-attachments/assets/b6132485-2b8f-481b-ac02-ca27ae9c0385)

## 2.  Georeference your map in Allmaps Editor

1. Open Allmaps Editor: [https://editor.allmaps.org](https://editor.allmaps.org)
2. Paste your IIIF manifest link into the text box and click “Load”

![Screenshot showing the ALlmaps Editor input box.](https://github.com/user-attachments/assets/2dcc5286-2423-49b1-8332-4f8d3ac9b168)

### Create Mask *(optional)*

On the next page, click “Mask”

 - In this step you are selecting the part of the image with the map and masking out the rest. **This step is optional, depending on your map.**

![Screenshot showing location of Mask button.](https://github.com/user-attachments/assets/30f04b3c-7634-45b9-b4bc-21527181001c)

1. Click to add points outlining the part of the map you wish to use
2. Complete the mask by clicking on the initial point to “close the loop”. 

![Screenshot showing completed mask.](https://github.com/user-attachments/assets/fdc5f526-8054-41c8-9a2f-88f29c779091)

### Georeference the map

1. Click on “Georeference”
2. Select a location on the “real world” in the window to the right, then select the corresponding point on the map in the window on the left. You have now created a ground control point or GCP! 
3. Do this 4-6 times, choosing points at locations spread about the map’s area. (You may need more points, depending on how much the map image must be deformed to match with reality.)
   
![Screenshot 2024-12-16 at 12 50 53 PM](https://github.com/user-attachments/assets/6e2c12c5-74ac-43d0-8fb0-72e7887ea3ba)

4. Click “Results”
5. Copy the URL at the end of the page

![Screenshot 2024-12-16 at 12 52 08 PM](https://github.com/user-attachments/assets/049b419a-d844-4a5a-8122-d582ff292ea4)

## 3.  Place Georeferenced Map in a Map Layer using Leaflet
*To create a webpage in which the Leaflet map will be displayed, we are using GitHub Pages, the same platform underpinning this tutorial and blog.* 

### Set up your repository and GitHub Page
- Create a new GitHub Repository for your webmap project. Mine is called ["leaflet"](https://github.com/kristinallarsen/leaflet)
- Create and publish a GitHub Page in the repository. Mine is called ["leaflet_iiif_allmapsxyz.html"](https://kristinallarsen.github.io/leaflet/leaflet_iiif_allmapsxyz.html)
  - [Quick Start guide for creating and configuring a GitHub Page](https://docs.github.com/en/pages/quickstart)
- Install the transparency slider plugin files in your repository
  - I downloaded the whole "lib" directory from the repository below and uploaded it to my "leaflet" repository. I'm sure there's a better way to do this :)
  - [Transparency slider code Leaflet Plugin](https://github.com/lizardtechblog/Leaflet.OpacityControls/tree/master)

### Start building the html for your page
Here is my html for the page through the end of the head section. 
*Note that the links to Leaflet CSS and JS are absolute links to their server, whie the CSS and JS for the opacity slider are relative links to my local installation of fhe files.* 

```

<!DOCTYPE html>
<html>
<head>
<title>Leaflet PLUS ALLMAPS XYZ</title>
<!-- Leaflet CSS and JS -->
<link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css"
     crossorigin=""/>
 <script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js"
     crossorigin="">
    </script>

<!--JS and CSS for ControlOpacity plugin slider and buttons, installed in my Leaflet repository-->
<script src="lib/jquery/jquery-1.9.1.js"></script>
<script src="lib/jquery/jquery-ui-1.10.3.custom.min.js"></script>
<link rel="stylesheet" href="lib/jquery/jquery-ui-1.10.3.custom.min.css" />
<link rel="stylesheet" href="lib/opacity/Control.Opacity.css" />
<script src="lib/opacity/Control.Opacity.js"></script>

<!-- CSS for the map container -->
<style>
		html, body {
			height: 100%;
			margin: 0px;
		}
		.leaflet-container {
			height: 1000px;
			width: 1200px;
			max-width: 100%;
			max-height: 100%;
		}
	</style>

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>

```
### Continue building the page
- Add html for your webmap, following this tutorial from "Preparing the Page" through "Setting up the Map" (you can ignore everything after "Markers, circles, and polygons" for now).
   - [Quick Start guide tutorial for creating a Leaflet webmap](https://leafletjs.com/examples/quick-start/)
- Define a second layer for your Allmaps xyz tile, replacing URL with the link you copied in Step 5 above  
- OR just copy my code, in which I defined the map container, an Open Street Map layer, and the Allmaps layer with const declarations and then called both layers into the map (again, replace my Allmaps link with yours, and replace the center point per the comment)

```
<body>
<div id="map" style="width: 1200px; height: 1000px;"></div>
<script>
// Initialize the map and set its view to a specific center point and zoom level. 
// Choose center point coordinates that correspond to the center of the historical map you are using.
// Allmaps tile server currently only supports one zoom level; here we set it to 13.
const map = L.map('map', {
  center: [37.757144, -122.443657], // San Francisco
  zoom: 13,
});

// Define the OpenStreetMap tile layer
const OpenStreetMap = L.tileLayer('https://tile.openstreetmap.org/{z}/{x}/{y}.png', {
  maxZoom:13,
  attribution:
    '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'
});
// Define the georeferenced historical map tile layer from Allmaps Editor. We've named this "AllMaps"
const AllMaps = L.tileLayer('https://allmaps.xyz/images/ad87bd6513550e53/{z}/{x}/{y}@2x.png', {
  maxZoom:13,
  attribution:
    '&copy; <a href="https://allmaps.xyz">Allmaps</a> contributors'
});

// Add the OpenStreetMap and AllMaps layers to the map
OpenStreetMap.addTo(map);
AllMaps.addTo(map);

```

### Add code for the opacity controller

If you have called your Allmaps layer something different you will need to change the code to match in the last line below.

```
// Add the ControlOpacity plugin controls
var higherOpacity = new L.Control.higherOpacity();
map.addControl(higherOpacity);
var lowerOpacity = new L.Control.lowerOpacity();
map.addControl(lowerOpacity);
var opacitySlider = new L.Control.opacitySlider();
map.addControl(opacitySlider);
higherOpacity.setOpacityLayer(AllMaps);

```

### Complete the page

Close the script, body, and html containers

```
</script>

</body>
</html>

```


Here's the full html code of the page

```

<!DOCTYPE html>
<html>
<head>
<title>Leaflet PLUS ALLMAPS XYZ</title>
<!-- Leaflet CSS and JS -->
<link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css"
     crossorigin=""/>
 <script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js"
     crossorigin="">
    </script>

<!--JS and CSS for ControlOpacity plugin slider and buttons, installed in my Leaflet repository-->
<script src="lib/jquery/jquery-1.9.1.js"></script>
<script src="lib/jquery/jquery-ui-1.10.3.custom.min.js"></script>
<link rel="stylesheet" href="lib/jquery/jquery-ui-1.10.3.custom.min.css" />
<link rel="stylesheet" href="lib/opacity/Control.Opacity.css" />
<script src="lib/opacity/Control.Opacity.js"></script>

<!-- CSS for the map container -->
<style>
		html, body {
			height: 100%;
			margin: 0px;
		}
		.leaflet-container {
			height: 1000px;
			width: 1200px;
			max-width: 100%;
			max-height: 100%;
		}
	</style>

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>


<body>
<div id="map" style="width: 1200px; height: 1000px;"></div>
<script>
// Initialize the map and set its view to a specific center point and zoom level. 
// Choose center point coordinates that correspond to the center of the historical map you are using.
// Allmaps tile server currently only supports one zoom level; here we set it to 13.
const map = L.map('map', {
  center: [37.757144, -122.443657], // San Francisco
  zoom: 13,
});

// Define the OpenStreetMap tile layer
const OpenStreetMap = L.tileLayer('https://tile.openstreetmap.org/{z}/{x}/{y}.png', {
  maxZoom:13,
  attribution:
    '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'
});
// Define the georeferenced historical map tile layer from Allmaps Editor. We've named this "AllMaps"
const AllMaps = L.tileLayer('https://allmaps.xyz/images/ad87bd6513550e53/{z}/{x}/{y}@2x.png', {
  maxZoom:13,
  attribution:
    '&copy; <a href="https://allmaps.xyz">Allmaps</a> contributors'
});

// Add the OpenStreetMap and AllMaps layers to the map
OpenStreetMap.addTo(map);
AllMaps.addTo(map);

// Add the ControlOpacity plugin controls
var higherOpacity = new L.Control.higherOpacity();
map.addControl(higherOpacity);
var lowerOpacity = new L.Control.lowerOpacity();
map.addControl(lowerOpacity);
var opacitySlider = new L.Control.opacitySlider();
map.addControl(opacitySlider);
higherOpacity.setOpacityLayer(AllMaps);

</script>

</body>
</html>

```



