---
title: "Topynym Extraction Workflow"
date: 2026-10-02
categories:
  - Blog
tags:
  - teaching
  - iiif
  - libraries
header:
  teaser: /assets/images/toponym.jpg
---

# Toponym Extraction Workflow Screenshots
 
This document provides a step-by-step guide for extracting toponyms from historical maps using various tools and platforms, including Internet Archive, Allmaps Editor, and Toponym Extractor.

1\. Start with a non-georeferenced image that has been processed with MapReader and the geoJSON resulting from that processing. If the image is already hosted with a IIIF service like Stanford’s SDR or [DavidRumsey.com](http://davidrumsey.com), skip to [step 2.](https://scribehow.com/o/rjZRmOedTHyhecnw_np_SQ/viewer/Toponym_Extraction_Workflow_Screenshots__M9KRteEnR3KPpH5hM8sXxw?scrollToActionId=d6befee3)

![](https://colony-recorder.s3.us-west-1.amazonaws.com/files/2026-10-02/ce1494c3-f799-4b73-ae7b-0a427fab1199/matched_image_action_0_704f276459914676bc3f2b6bd4d9ccca_text_export.jpeg)


2\. Upload image(s) to Internet Archive to create a IIIF manifest.

**Get help**\
Get Started with IIIF on Internet Archive guide: <https://iiif.io/guides/guides/archive.org/>\
Generate IIIF manifests from IA links: <https://kristinallarsen.github.io/IIIFmanifest_maker/>

**Examples**\
Item page created via upload: <https://archive.org/details/carte-de-l-afrique-occidentale-francaise-dressee-par-a.-meunier-et-e.-barralier-> \
IIIF manifest derived from IA URL: <https://iiif.archive.org/iiif/carte-de-l-afrique-occidentale-francaise-dressee-par-a.-meunier-et-e.-barralier-/manifest.json>

![](https://colony-recorder.s3.us-west-1.amazonaws.com/files/2026-10-02/3446e1ff-84b1-43fd-9a0f-bf6dbcaea4a3/matched_image_action_1_b624c5938e4f4caa93565b3e65013897_text_export.jpeg)


3\. Georeference image in Allmaps Editor with IIIF Manifest.

Allmaps Editor: [https://editor.allmaps.org/](https://editor.allmaps.org/?lang=en) \
Paste IIIF manifest (from IA or elsewhere) into text box and click return. 

Georeferencing Tutorial: [Georeferencing with Allmaps tutorial](https://kristinalivlarsen.com/blog/georeferencing_tutorial/)

Be sure to draw a mask around the map area. The Toponym Extractor will exclude any points located outside of the mask, eliminating results from legends, scale, notes, etc.

![](https://colony-recorder.s3.us-west-1.amazonaws.com/files/2026-10-02/fba1b2f0-64fc-445f-a74a-86d5d491f97a/matched_image_action_3_130126b8cd8b47f492638b350b8de37c_text_export.jpeg)


4\. Click “Export” in the upper right of the Results page to show link to Georeference Annotation.

![](https://colony-recorder.s3.us-west-1.amazonaws.com/files/2026-10-02/c4fc6120-404e-4b1e-b60c-b3ffc07fe043/matched_image_action_4_6611d293e2da47d89e9520e0d0311dbb_text_export.jpeg)


5\. Upload geojson to Toponym Extractor in “MapReader Detections” card. Paste Allmaps Georeference Annotation link and click Fetch.

![](https://colony-recorder.s3.us-west-1.amazonaws.com/files/2026-10-02/5955f3f0-fec1-4b43-a5d7-5b1875298575/matched_image_action_5_4a13485e38934df9a22f5f68bfb54005_text_export.jpeg)


6\. Set options as desired. \
\
(Recommended: leave "Discard detections outside the mask" checked, set confidence score high to drop noise, leave others as-is). 

Click Convert to lat/long.

![](https://colony-recorder.s3.us-west-1.amazonaws.com/files/2026-10-02/33224b52-5711-46f0-b167-522814595728/matched_image_action_6_9f5f430def6149ca8d407b565e9326b0_text_export.jpeg)


7\. Scroll down to reveal Results. \
Click “Show map preview” to open the map viewer. \
Toggle historical map image on and off with the transparency slider.

![](https://colony-recorder.s3.us-west-1.amazonaws.com/files/2026-10-02/412947c4-5765-4a2c-951f-ed57fe1a254a/matched_image_action_7_00269b6cb55c4878a893533862d4b8fa_text_export.jpeg)


8\. Tabular results below the map viewer can be sorted by clicking column headings. \
Export data file by clicking “Download CSV”.

![](https://colony-recorder.s3.us-west-1.amazonaws.com/files/2026-10-02/09401265-78e6-426f-a6f4-b9e75c4d1604/matched_image_action_8_a725eff9a29449d5b613c5d55c885b78_text_export.jpeg)


9\. Optional: upload csv to google sheets or open locally in Excel.

![](https://colony-recorder.s3.us-west-1.amazonaws.com/files/2026-10-02/d7e19aed-c8c7-4604-b402-84ccb30057c9/matched_image_action_9_4dada5b43a47483a819795114e81ede5_text_export.jpeg)


10\. Data file can be opened and plotted in GIS software, and the georeferenced map image can be added via Allmaps XYZ tiles. \
\
Example 1: [Felt.com](http://felt.com) <https://felt.com/map/testing-topomyn-extraction-TXKFMP3qR9C9BqYTnmDO2ibA?loc=8.181,-12.281,7.45z>

![](https://colony-recorder.s3.us-west-1.amazonaws.com/files/2026-10-02/a04c7b97-f2cc-480f-a5a2-4a7dfbd6f38d/matched_image_action_10_6f347a135653495c8a002009a76ff778_text_export.jpeg)


11\. Example 2: ArcGIS Online <https://stanford.maps.arcgis.com/apps/mapviewer/index.html?webmap=90d4538ddac648de8cee30088ec8b31e>

![](https://colony-recorder.s3.us-west-1.amazonaws.com/files/2026-10-02/f385c9fc-a921-4130-87db-2a7e925cd0c7/matched_image_action_11_7de44779bba3497ba4d4fb769fda0d50_text_export.jpeg)
