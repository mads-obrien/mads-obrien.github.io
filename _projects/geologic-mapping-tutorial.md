---
name: Tutorial - Geologic Mapping with ArcGIS
tools: [arcgis, stanford, tutorial, writing]
image: /myassets/thumbnail_geologic_tutorial.png
description: A guide for creating geologic maps using the USGS NCGMP09 cartographic standards.
---

## Geologic Mapping with ArcGIS ##
#### *A self-paced ArcMap tutorial for geologists*

![A photo](http://placekitten.com/700/375)

{% include elements/button.html link="/myassets/Geologic-Mapping-with-EsriNCGMP-nocomments.pdf" text="View tutorial PDF" style="primary" size="sm" %}
{% include elements/button.html link="/myassets/WorkshopData.zip" text="Download tutorial data .zip" style="primary" size="sm" %}  

*Duration:* Oct 2019 - Dec 2019  
*Affiliation:* Stanford Geospatial Center  
*What:* GIS tutorial (instructions and test data)  
*My Role:* Tutorial author


### The Task:

The Stanford Geospatial Center offers a few intro GIS [workshops](https://library.stanford.edu/research/stanford-geospatial-center/workshops) focusing on raster and vector operations. However, the Director of Field Education at the Stanford School of Earth approached me about creating a small course that would be a “second step” for its geology students, who would have taken the intro GIS workshop but not much else. The audience of the workshop are students who may have created detailed field notes or paper maps, but want to create a digital version.


### My Approach:

I relied heavily on my previous geology education to decide what items one might sketch on a paper map that one would want to know how to include digitally.

To make mapping as “plug and play” as possible, and to help students create a map easily understood by other professionals, I based my tutorial on the NCGMP09 geologic mapping standard, a standardized set of symbols for geologic features developed by the USGS National Cooperative Geologic Mapping Program. *(NOTE: This tutorial was written prior to the 2020 adoption of [GeMS](https://doi.org/10.3133/tm11B10) as USGS's new standardized geologic map schema.)* My instructions teach students how to download this map template in the form of a geodatabase, and how to enter their field data into the feature classes of the template. 

I also didn't want to totally re-invent the wheel: the tutorial is partially based on a short course by [Ralph Haugerud (USGS)](https://ngmdb.usgs.gov/Info/standards/NCGMP09/) and workshop material created by [Roman DiBiase and Erin DiMaggio (Penn State Geosciences)](http://sites.psu.edu/dibiase/teaching/making-a-geologic-map-in-arcgis-10-x/).

### Outcome highlights:  

The final tutorial constructs a hypothetical geologic map of a site regularly visited by students in Stanford's Wrigley Field Program, tracing geologic contacts based on aerial imagery and field observation points.

![A photo](/myassets/geomap-screenshot.png)

Some topics covered include:
* Creating subtypes within feature classes, and setting default attribute values for new features
* Adding XY data collected from a field GPS unit
* Creating topology files that mirror the rules of geologic mapping and checking for topology errors within a geodatabase
* Using cartographic representation files to simplify map symbology
* Making VBScript expressions for custom feature labels
* Systematically rotating point symbols based on a "degrees" attribute field (i.e. strike and dip markers)
* Introduce users to USGS mapping and symbology standards 


<< [Back to Projects](/projects/)