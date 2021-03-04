---
name: Tutorial - Geologic Mapping with ArcGIS
tools: [arcgis, earth science, tutorial, writing]
image: /myassets/thumbnail_geologic_tutorial.png
description: A guide for creating geologic maps using the USGS NCGMP09 cartographic standards.
---

## Geologic Mapping with ArcGIS ##
#### *A self-paced ArcMap tutorial for geologists*

![A photo](http://placekitten.com/700/375)

{% include elements/button.html link="/myassets/Geologic-Mapping-with-EsriNCGMP-nocomments.pdf" text="View tutorial PDF" style="primary" size="sm" %}
{% include elements/button.html link="/myassets/WorkshopData.zip" text="Download tutorial data .zip" style="primary" size="sm" %}  

**Duration:** Oct 2019 - Dec 2019  
**Affiliation:** Stanford Geospatial Center  
**What:** GIS tutorial (instructions and test data)  
**My Role:** Tutorial author


### The Task:

The Stanford Geospatial Center offers a few introductory GIS [workshops](https://library.stanford.edu/research/stanford-geospatial-center/workshops), focusing on raster and vector operations. But the Director of Field Education at the Stanford School of Earth approached me about creating a “second step” workshop for its geology students. The target audience of the workshop would be students who'd created detailed field notes or handdrawn geologic maps, but wished to create a digital version and had only introductory GIS knowledge.


### My Approach:

I relied heavily on my previous geology education to distill the tutorial to the most common and/or most important features. *"What items might I sketch on a paper map that I'd need to include digitally?"*

To make mapping as “plug and play” as possible, and to help students create a map easily understood by other professionals, I based my tutorial on the **NCGMP09 geologic mapping standard**, a standardized set of symbols for geologic features developed by the USGS National Cooperative Geologic Mapping Program. *(NOTE: This tutorial was written prior to the 2020 adoption of [GeMS](https://doi.org/10.3133/tm11B10) as USGS's new standardized geologic map schema.)* My instructions teach students how to download this map template in the form of a geodatabase, and how to enter their field data into the feature classes of the template. 

I also didn't want to totally re-invent the wheel: the tutorial is partially based on a short course by [Ralph Haugerud](https://ngmdb.usgs.gov/Info/standards/NCGMP09/) (USGS) and workshop material created by [Roman DiBiase and Erin DiMaggio](http://sites.psu.edu/dibiase/teaching/making-a-geologic-map-in-arcgis-10-x/) (Penn State Geosciences).

### Outcome highlights:  

The tutorial constructs a hypothetical geologic map of a site regularly visited by Stanford's Wrigley Field Program, tracing geologic contacts based on aerial imagery and field observation points.

![A photo](/myassets/geomap-screenshot.png)

Some topics covered include:
* Creating subtypes within feature classes and setting default attribute values for new features
* Adding XY data collected from a field GPS unit
* Creating topology files that mirror the rules of geologic mapping and checking for topology errors within a geodatabase
* Using cartographic representation files to simplify map symbology
* Making VBScript expressions for custom feature labels
* Systematically rotating point symbols based on a "degrees" attribute field (i.e. strike and dip markers)
* Introduce users to USGS mapping and symbology standards 


<< [Back to Projects](/projects/)