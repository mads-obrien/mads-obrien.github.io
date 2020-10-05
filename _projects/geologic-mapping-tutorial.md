---
name: Geologic Mapping with ArcGIS Tutorial
tools: [arcgis, stanford, tutorial, writing]
image: /myassets/thumbnail_geologic_tutorial.png
description: A guide for creating geologic maps using the USGS NCGMP09 cartographic standards.
---

## Title of Project ##

![A photo](http://placekitten.com/400/375)

{% include elements/button.html link="/myassets/Geologic-Mapping-with-EsriNCGMP-nocomments.pdf" text="View tutorial PDF" style="primary" size="sm" %}
{% include elements/button.html link="/myassets/WorkshopData.zip" text="Download tutorial data .zip" style="primary" size="sm" %}


*Duration:* Oct 2019 - Dec 2019  
*Affiliation:* Stanford Geospatial Center  
*What:* GIS tutorial (instructions and test data) 
*My Role:* Tutorial author


### The Task:

I was approached by XXXX in the Stanford Earth department. The Stanford GIS center offers a few intro GIS workshops focusing on raster and vector projects, but the School of Earth was interested in a small course that would be a “second step” after the intro prerequisite for its geology students. The assumptions about the audience are that they will have taken our intro GIS workshop but not much else. Students in the School of Earth will occasionally go on field trips to collect data, then create a digital version of the field mapping they did on paper / on location.
Goal was for the tutorial to last about 3 hours.

I saw this tutorial as having two primary goals -- teaching non GIS experts how to use this (somewhat complicated) ESRI template... but also teach them how to execute the most popular or most common tasks to someone creating a geologic map. I relied heavily on my past geology education to ask myself, "What are the bare minimum skills I would want to know how to do on a geologic map, that I would normally include on a paper geologic map?"

### My Approach:

To make this mapping as “plug and play” as possible, and to help these students create not just any old geologic map but one that follows the guidelines recognized by government and academic geologists, I based my tutorial on following the _____ template designed by the USGS and the NCGKEHDE. *(NOTE: Since the authoring of this tutorial, the new standard is the GEMS framework.)* My instructions teach students how to download this template, in the form of a geodatabase, and enter their field data into the feature classes of the template.
Introduces students to the handbook for picking geologic map symbology and colors.
Based off a combination of these tutorials: Ralph Hauregard and .....Penn State person

I also didn't want to totally re-invent the wheel: the tutorial is partially based on workshop material created by [Roman DiBiase and Erin DiMaggio (Penn State Geosciences)](http://sites.psu.edu/dibiase/teaching/making-a-geologic-map-in-arcgis-10-x/) and a short course by [Ralph Haugerud (USGS)](https://ngmdb.usgs.gov/Info/standards/NCGMP09/).



### Outcome highlights:  

* Tutorial uses field data from a site in Hawaii that Stanford Earth has taken students before—plus there is interesting geology and variation there which is good to illustrate in 
* Talks about two methods for mapping – tracing geologic contacts based on aerial imagery and field observation points, as well as digitizing geologic maps into shapefiles.
* Personally became familiar with USGS mapping and symbology standards 
* Teaches users simply about topics such as:
- agreement of feature classes within a database (coordinate system, topology)
- creating subtypes within feature classes, and filling in default attribute values
- creating topology files and checking for topology errors
- using cartographic representation files (to expedite symbology following existing standards)
- adding xy data of GPS data collected from a field unit
- Making VBScript expressions for custom feature labels
- systematically rotating point symbols based on a "degrees" attribute field (i.e. strike and dip markers)




<< [Back to Projects](/projects/)