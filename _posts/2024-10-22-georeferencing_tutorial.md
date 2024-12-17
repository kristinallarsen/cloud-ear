---
title: "Tutorial: IIF > Allmaps Editor > Felt.com"
excerpt_separator: "<!--more-->"
categories:
  - Blog
tags:
  - Post Formats
  - readability
  - standard
---
# How to Georeference a Map in Allmaps to Display in Felt
*A step-by-step tutorial on how to georeference a map from DavidRumsey.com or Searchworks.edu using Allmaps Editor and then display it in a webmap on Felt.com.*
<!--more-->
## Background Info

- What is georeferencing?
[https://blogs.loc.gov/maps/2021/01/georeferencing-moving-analog-maps-into-modern-day-gis/](https://blogs.loc.gov/maps/2021/01/georeferencing-moving-analog-maps-into-modern-day-gis/)

- What is a IIIF Manifest?
[https://iiif.io/guides/using_iiif_resources/#what-is-a-iiif-manifest](https://iiif.io/guides/using_iiif_resources/#what-is-a-iiif-manifest)

- What is Allmaps?
[https://allmaps.org/](https://allmaps.org/)

- What is Felt? 
[https://felt.com/about](https://felt.com/about)

- What else can you do with Felt? 
[https://help.felt.com](https://help.felt.com)


## 1.  Get Started: Locate and copy a IIIF manifest link for your map

*IIIF manifest links can be found on many digital repository and library sites. Unfortunately, there’s not much standardization across sites as to where to put them in a record, so you may have to dig around for them. Below are screenshots of where to find manifest links on David Rumsey’s website and in Stanford’s Searchworks library catalog.*

***You do not need to get a link from both places, just choose one to use, copy it, and move to step 2.***

### A. Find IIIF Manifest on Davidrumsey.com:

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

1. Open Allmaps Editor: https://editor.allmaps.org
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

## 3.  Place Georeferenced Map in a Map Layer in Felt.com 

*There are other options for this step, like ArcGIS Online and QGIS, among others, but Felt.com is very easy for beginners. You can sign up for a trial membership and/or request a free educational license from an .edu email address.*

### Make a New Map and Upload URL

1. Click on “New Map” in the upper right corner
   
![Screenshot 2024-12-16 at 3 51 26 PM](https://github.com/user-attachments/assets/f6715fae-6ba8-4b74-b6c9-ec20aa8074a9)

2. In the new map, click on the Felt logo in the upper left and find “Upload by URL” in the dropdown menu

![Screenshot 2024-12-16 at 3 52 05 PM](https://github.com/user-attachments/assets/04af5969-c58d-4911-aaa5-7c2e9794ac87)

3. Paste the URL you created in step 2 in the pop-up box and click “Add to map”

![Screenshot 2024-12-16 at 3 52 36 PM](https://github.com/user-attachments/assets/c9f74e1e-81ca-45f5-bf9e-133736f23a30)

4. You will probably have to manually zoom to the place where your map should be the first time you view it.

### Style and Name Map Elements

1. Click on the Legend pane in the upper left to open the Style menu on the right. You can rename your layer in the place indicated by the arrow below. You can change the opacity of the map in that menu as well. Give your map a name by double-clicking on “Untitled Map” in the upper left corner and typing it in.

![Screenshot 2024-12-16 at 3 53 51 PM](https://github.com/user-attachments/assets/18619cb5-4f42-4bc9-9fb4-59e1ec9ba2c5)

2. You can now create additional layers and import other data or create your own points, lines, and polygons. See Felt documentation for more information: [https://help.felt.com](https://help.felt.com)

### Map after renaming file and layer:

![Screenshot 2024-12-16 at 3 54 53 PM](https://github.com/user-attachments/assets/a8e41ffa-49ff-4201-a67f-2f80824ab229)


[View this map in Felt](https://felt.com/map/San-Antonio-Heights-rvyY9CjDYTiC7CzFzS10EiA?loc=34.155614,-117.655922,15.48z&share=1) 







