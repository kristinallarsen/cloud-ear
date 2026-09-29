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

<iframe src="https://docs.google.com/document/d/e/2PACX-1vQIincuK7XVyd1maS_vf72_ROt5AVKO6KQ4PhetZfCpYU49KPOx2DrlueHIIkujqTBdjMnrAPSdSA8P/pub?embedded=true"></iframe>

Quick Links:

<ul>
  <li>Open App: [https://davidrumseymapcenter.github.io/toponym-extractor/](https://davidrumseymapcenter.github.io/toponym-extractor/)</li>
  <li>Download (right click and save) sample [geojson file with text annotations](assets/P. Famin_Carte_du_Cayor et du_Diambour_1883.geojson)</li>
  <li>Upload that file in card one, **MapReader detections**</li>
  <li>Paste this Allmaps Georeference Annotation link in card two: https://annotations.allmaps.org/images/cb2700e9d323cd85 and click Fetch</li>
  <li>Scroll down and click Convert to lat/long</li>
  <li>View results on webmap with Show map preview button</li>
</ul>
