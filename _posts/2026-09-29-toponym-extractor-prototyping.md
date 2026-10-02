---
title: "Topynym Extractor"
date: 2026-09-29
categories:
  - Blog
tags:
  - teaching
  - iiif
  - libraries
header:
  teaser: /assets/images/toponym.jpg
---

<img src="/assets/images/topopnym.jpg" alt="" />

## Deriving lat/long coordinates from pixel-based text annotations

This [vibe-coded app](https://davidrumseymapcenter.github.io/toponym-extractor/) turns MapReader text detections in pixel coordinates into a downloadable csv file with latitude/longitude, using the ground control points in an Allmaps Georeference Annotation. 

More info and documentation to come on this one, but for now here's a quick way for you to demo.

## Quick Demo

Open App in a new tab: [Toponym Extractor](https://davidrumseymapcenter.github.io/toponym-extractor/)

Download (right click and save) sample [geojson file with text annotations](/assets/P_Famin_Carte_du_Cayor_et_du_Diambour_1883.geojson). 

Upload that file in card one, **MapReader detections**

Paste this **Allmaps Georeference Annotation** link in card two and click "Fetch": 

```
https://annotations.allmaps.org/images/cb2700e9d323cd85
```
  
Scroll down and click "Convert to lat/long"

View results on webmap with "Show map preview" button

--- 

## Learn More

View a more detailed [workflow with screenshots](https://docs.google.com/document/d/e/2PACX-1vQIincuK7XVyd1maS_vf72_ROt5AVKO6KQ4PhetZfCpYU49KPOx2DrlueHIIkujqTBdjMnrAPSdSA8P/pub). 
