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

# Toponym Extraction workflow

*work in progress -- images still to come*

## Start with a non-georeferenced image that has been processed with MapReader and the geoJSON resulting from that processing

If the image is already hosted with a IIIF service like Stanford’s SDR or [DavidRumsey.com](http://DavidRUmsey.com), skip to step 2\.  

1. ## Upload image(s) to Internet Archive to create a IIIF manifest

Get Started with IIIF on Internet Archive guide: [https\://iiif.io/guides/guides/archive.org/](https://iiif.io/guides/guides/archive.org/)   
Generate IIIF manifests from IA links: [https\://kristinallarsen.github.io/IIIFmanifest\_maker/](https://kristinallarsen.github.io/IIIFmanifest_maker/) 

![][image1]  
Item page: [https\://archive.org/details/carte-de-l-afrique-occidentale-francaise-dressee-par-a.-meunier-et-e.-barralier-](https://archive.org/details/carte-de-l-afrique-occidentale-francaise-dressee-par-a.-meunier-et-e.-barralier-)

IIIF manifest:  
[https\://iiif.archive.org/iiif/carte-de-l-afrique-occidentale-francaise-dressee-par-a.-meunier-et-e.-barralier-/manifest.json](https://iiif.archive.org/iiif/carte-de-l-afrique-occidentale-francaise-dressee-par-a.-meunier-et-e.-barralier-/manifest.json)

2. ## Georeference image in Allmaps Editor with IIIF Manifest

Allmaps Editor: [https\://editor.allmaps.org/](https://editor.allmaps.org/?lang=en)  
Paste IIIF manifest (from IA or elsewhere) into text box and click return.  
[Georeferencing with Allmaps tutorial](https://kristinalivlarsen.com/blog/georeferencing_tutorial/) 

- follow steps 1-2, app has been updated so screenshots no longer match  

## ![][image2]

Note: Draw a mask around the map area. The Toponym Extractor will exclude any points located outside of the mask, eliminating results from legends, scale, notes, etc.

[https\://editor.allmaps.org/results?url=https%3A%2F%2Fiiif.archive.org%2Fiiif%2Fcarte-de-l-afrique-occidentale-francaise-dressee-par-a.-meunier-et-e.-barralier-%2Fmanifest.json\&image=https%3A%2F%2Fiiif.archive.org%2Fimage%2Fiiif%2F3%2Fcarte-de-l-afrique-occidentale-francaise-dressee-par-a.-meunier-et-e.-barralier-%252FCarte\_de\_l\_Afrique\_occidentale\_franc%25CC%25A7aise\_-\_dresse%25CC%2581e\_par\_A.\_Meunier\_et\_E.\_Barralier%2C\_1903\_\_\_Ministe%25CC%2580re\_des\_colonies.\_Service\_ge%25CC%2581ographique\_et\_des\_missions.\_M.\_Barbotin%2C\_chef\_du\_service\_-\_btv1b530605988\_%284\_of\_6%29.jpg](https://editor.allmaps.org/results?url=https%3A%2F%2Fiiif.archive.org%2Fiiif%2Fcarte-de-l-afrique-occidentale-francaise-dressee-par-a.-meunier-et-e.-barralier-%2Fmanifest.json&image=https%3A%2F%2Fiiif.archive.org%2Fimage%2Fiiif%2F3%2Fcarte-de-l-afrique-occidentale-francaise-dressee-par-a.-meunier-et-e.-barralier-%252FCarte_de_l_Afrique_occidentale_franc%25CC%25A7aise_-_dresse%25CC%2581e_par_A._Meunier_et_E._Barralier%2C_1903___Ministe%25CC%2580re_des_colonies._Service_ge%25CC%2581ographique_et_des_missions._M._Barbotin%2C_chef_du_service_-_btv1b530605988_%284_of_6%29.jpg)

Click “Export” in the upper right of the Results page to show link to Georeference Annotation

3. ## Upload geojson to Toponym Extractor in “MapReader Detections” card. Paste Allmaps Georeference Annotation link and click Fetch. 

![][image3]

4. ## Set options as desired. (Recommended: leave Discard detections outside the mask checked, set confidence score high to drop noise, leave others as-is). Click Convert to lat/long

## ![][image4]

5. ## Scroll down to reveal Results. Click “Show map preview” to open the map viewer. Toggle historical map image on and off with the transparency slider. Tabular results below the map viewer can be sorted by clicking column headings. Export data file by clicking “Download CSV” 

   

![][image5]  
![][image6]

6. ## Optional: upload csv to google sheets or open locally in Excel.

![][image7]  
[Meunier et Barralier sheet 4 of 6](https://docs.google.com/spreadsheets/d/1YvK7tCnBn7l4U8oc51NhaCkqbLF3dSVDSGMAQH3McF0/edit?gid=1134780325#gid=1134780325)

7. ## Data file can be opened and plotted in GIS software. Georeferenced map image can be added via Allmaps XYZ tiles 

### Example: [Felt.com](http://Felt.com)

[https\://felt.com/map/testing-topomyn-extraction-TXKFMP3qR9C9BqYTnmDO2ibA?loc=8.181,-12.281,7.45z](https://felt.com/map/testing-topomyn-extraction-TXKFMP3qR9C9BqYTnmDO2ibA?loc=8.181,-12.281,7.45z)

## [![][image8]](https://felt.com/map/testing-topomyn-extraction-TXKFMP3qR9C9BqYTnmDO2ibA?loc=8.181,-12.281,7.45z)

### Example: ArcGIS Online

[https\://stanford.maps.arcgis.com/apps/mapviewer/index.html?webmap=90d4538ddac648de8cee30088ec8b31e](https://stanford.maps.arcgis.com/apps/mapviewer/index.html?webmap=90d4538ddac648de8cee30088ec8b31e)   
[![][image9]](https://stanford.maps.arcgis.com/apps/mapviewer/index.html?webmap=90d4538ddac648de8cee30088ec8b31e%20)
 
