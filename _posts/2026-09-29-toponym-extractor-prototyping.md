---
title: "Topynym Extractor"
date: 2026-09-29
categories:
  - Blog
tags:
  - teaching
  - iiif
  - libraries
---
## Deriving lat/long coordinates from pixel-based text annotations

This [vibe-coded app](https://davidrumseymapcenter.github.io/toponym-extractor/) turns MapReader text detections in pixel coordinates into a latitude/longitude table, using the ground control points in an Allmaps Georeference Annotation. 

More info and documentation to come on this one, but for now here's a workflow with screenshots:

<iframe src="https://docs.google.com/document/d/e/2PACX-1vQIincuK7XVyd1maS_vf72_ROt5AVKO6KQ4PhetZfCpYU49KPOx2DrlueHIIkujqTBdjMnrAPSdSA8P/pub?embedded=true" frameborder="0" width="569" height="960" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

Quick Links:

Open App:[vibe-coded app](https://davidrumseymapcenter.github.io/toponym-extractor/)

Download (right click and save) sample [geojson file with text annotations]([assets/P. Famin_Carte_du_Cayor et du_Diambour_1883.geojson](https://github.com/kristinallarsen/cloud-ear/blob/master/assets/P.%20Famin_Carte_du_Cayor%20et%20du_Diambour_1883.geojson)) 

Upload that file in card one, **MapReader detections**

Paste this **Allmaps Georeference Annotation** link in card two: https://annotations.allmaps.org/images/cb2700e9d323cd85 and click "Fetch"
  
Scroll down and click "Convert to lat/long"

View results on webmap with "Show map preview" button

