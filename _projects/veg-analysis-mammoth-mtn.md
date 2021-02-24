---
name: Historical Image Analysis of Tree Mortality at Horseshoe Lake
tools: [arcgis, data analysis, geoprocessing, photogrammetry, python, remote sensing]
image: /myassets/thumbnail_mammoth_mtn.jpg
description: I conducted supervised image classification of aerial photos (1951-2014) to quantify deforestation on Mammoth Mountain, CA.
---

## Historical Image Analysis of Tree Mortality at Horseshoe Lake ##

{% capture carousel_images %}
https://bit.ly/2BBbVhc
https://bit.ly/2DOtxXB
{% endcapture %}
{% include elements/carousel.html %}

{% include elements/button.html link="https://agu.confex.com/agu/fm16/meetingapp.cgi/Paper/136618" text="Read abstract (AGU)" style="primary" size="sm" %}

**Duration:** June 2016 - October 2017  
**Affiliation:** US Geological Survey  
**What:** Federal research project   
**My Role:** Intern-turned-employee, and occasional field assistant  


### The Task ###

I joined the USGS Menlo Park office as a [NAGT intern](https://nagt.org/nagt/students/usgs_field.html) upon my college graduation. 


 Aerial photography allows us to compare the state of vegetation at HSL before and after diffuse CO2 emissions are thought to have begun in 1990. The photos provide an especially valuable look at the site during the years before regular CO2 flux measurements began at HSL in 1995 (CITE THIS?)

To reinforce our interpretation of the imagery, we compare the photographs to spatial geochemical data showing the locations of CO2 hotspots over time (Werner et al, 2014) to find spatial patterns or correlations between CO2 spikes and localized pockets of dieoff. 

### Project Goals ###

ajsksmdksdkjlsdkljff


### My Approach ###

Experimented with various methods of image classification with historical photographs, including  (making the images black and white)

Sourced historical photographs from EROS EarthExplorer, the Map and Imagery Laboratory at UC Santa Barbara. 

Preliminary tests showed that different training signatures caused high variation between supervised classification results for the same image. To counteract this variation, we took an average of 1000 classifications of the same image.


To try and control for the effect of image artifacts on classification accuracy, we classified a separate control site (CS) in each of our respective images 1000 times, using the same 1000 signature files on which our HSL classifications were based. 

We assumed that the true bare area at CS was not changing over time and assumed that the mean of the 23 bare area estimates represented this “true” bare area. By comparing how much the classified BA for that image differed from the “true” CS amount, we calculated a positive or negative percent difference which could be attributed to image artifacts. We then adjusted each of our HSL BA estimates by this percent difference, which increased or decreased the estimate to compensate for under- or over-estimation of bare ground, respectively.



### Outcome Highlights ###

* Between 1951 and 1987 canopy cover at HSL remained relatively constant, with the area of bare ground beginning to increase in 1992. 
* Though on-the-ground observations seemed to indicate that the dieoff had stabilized by 2005, our results show more fluctuation in treeless area than expected since 2005, possibly due to significant plant regrowth and large windstorms causing tree fall. 
* Despite subsequent spikes in CO2 flux in the region, the footprint of the tree kill seemed to remain stable from 2001-2014.



* Gained lots of experience in manual georectification of historical imagery, and familiarity with the various warps used when georectifying
* Improved the classification accuracy from previous year
* Added XX new images to our historical image timeline.





<< [Back to Projects](/projects/)