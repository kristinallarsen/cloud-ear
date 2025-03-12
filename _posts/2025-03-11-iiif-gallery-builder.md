---
title: "Experiment: IIIF Gallery Builder"
date: 2025-03-11T18:00
categories:
  - Blog
tags:
  - teaching
  - maps
classes: wide
---

*Continued experiments with using ChatGPT to code a IIIF Gallery*

# Gallery Builder prototyping with ChatGPT

After my first chaotic experiment writing code with Chat GPT and publishing it to GitHub pages I regrouped and focused on creating a local version of the app, based on Evan Thornberry’s sage advice.  

This time ChatGPT and I (lol) came up with a simpler solution which does not require the use of a server to save and retrieve files, because you just download a JSON file of your gallery once created and upload it to view it again. 

This version also creates a combined manifest out of the individual manifests, instead of whatever the last iteration was trying (and failing) to do. 

It’s ugly but it works: 

[Link to page under development](https://kristinallarsen.github.io/gallery-builder/)

Right now, this can parse manifests from Stanford University Libraries, David Rumsey Map Collection, Digital Commonwealth, Library of Congress, and the Victoria and Albert Museum. 

There is much MUCH more to say about how every single institution is handling basic information like titles, dates, and authors in completely different ways in their manifests. 
 
Perhaps there is some logic at work that I don’t yet understand (is it because of the underlying information management systems?) but I thought the point of the IIIF Framework was consistency. 

Use the manifest links below to populate the gallery on the left. Click a thumbnail to open the image in the viewer pane on the right. 

```
https://collections.leventhalmap.org/search/commonwealth:t722qd86g/manifest,
https://collections.leventhalmap.org/search/commonwealth:8623r0577/manifest,
https://collections.leventhalmap.org/search/commonwealth:d217xv241/manifest,
https://www.davidrumsey.com/luna/servlet/iiif/m/RUMSEY~8~1~368087~90135375/manifest,
https://www.davidrumsey.com/luna/servlet/iiif/m/RUMSEY~8~1~281766~90054435/manifest,
https://iiif.vam.ac.uk/collections/O70207/manifest.json,
https://www.loc.gov/item/2006629341/manifest.json,

```

