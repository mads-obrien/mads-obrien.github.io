---
name: Historical Image Analysis of Tree Mortality at Horseshoe Lake
tools: [arcgis, data analysis, geoprocessing, photogrammetry, python, remote sensing]
image: /myassets/thumbnail_mammoth_mtn.jpg
description: I conducted supervised image classification of aerial photos (1951-2014) to quantify deforestation on Mammoth Mountain, CA.
---

## Historical Image Analysis of Tree Mortality at Horseshoe Lake ##

{% capture carousel_images %}
/myassets/20160715_HSLDeadStuff_750px.jpg
/myassets/20160715_HSLSign_750px.jpg
/myassets/20160717_BasaltCanyonHill_750px.jpg
{% endcapture %}

{% capture carousel_captions %}
Looking west at the Horseshoe Lake tree kill (July 2016)
Looking south at Horseshoe Lake tree kill abutting healthy forest (July 2016)
Tree and sage die-off at Basalt Canyon (July 2016)
{% endcapture %}

{% include elements/carousel.html %}

{% include elements/button.html link="https://agu.confex.com/agu/fm16/meetingapp.cgi/Paper/136618" text="Read conference abstract" style="primary" size="sm" %}
{% include elements/button.html link="/myassets/AGUPoster-OBrienMadeleine_EP21D-0905_Final.pdf" text="View conference poster (PDF)" style="primary" size="sm" %}

**Duration:** June 2016 - October 2017  
**Affiliation:** US Geological Survey  
**What:** Federal research project   
**My Role:** Intern-turned-employee, and occasional field assistant  


### The Task ###

I joined the USGS Menlo Park office as a [NAGT intern](https://nagt.org/nagt/students/usgs_field.html) upon my college graduation. The USGS/NAGT Cooperative Field Training Program matches top-performing recent grads with USGS research projects nationwide. I was matched with a photogrammetry and landscape change analysis project within a research group focusing on hydrothermal systems.

This project's study site was Horseshoe Lake, a recreation area southwest of Mammoth Mountain in Mono County, California. USGS scientists had been studying a unique case of tree dieoff there for a few years, caused by extremely high soil CO2 flux. (More info [here](https://www.usgs.gov/volcanoes/long-valley-caldera/long-valley-caldera-field-guide-horseshoe-lake?qt-science_support_page_related_con=4#qt-science_support_page_related_con).) 

My PIs and mentors wished to answer the questions, "How much barren area was present at Horseshoe Lake before magmatic CO2 flux became so high? How has the tree kill area changed over time, and what is the area of this tree kill today?"

{% include elements/figure.html image="/myassets/HSL_timeline_fromslides.jpg" caption="Timeline I created to summarize seismic, carbon flux, and tree kill events during a portion of the study period. Green indicates increased carbon dioxide flux, and Pink indicates decreased carbon dioxide flux. Sources: Cook et al, 2001; Lewicki et al, 2014. Slide is excerpted from talk I gave at the conclusion of my internship." %}

### Project Goals ###

* Acquire more photographs for the time series to be analyzed, especially those from pre-1990---to establish a vegetation baseline before regular CO2 monitoring of the site began.
* Develop a consistent image classification method for all the photographs, to quantify the area (m<sup>2</sup>) of barren ground caused by tree kill.
* Compare the photographs to spatial geochemical data showing the locations of CO2 hotspots over time (Werner et al, 2014) to find spatial patterns or correlations between CO2 spikes and localized pockets of dieoff. 

### My Approach ###

I experimented with many image classification methods to select the most suitable method for my historical photographs. This involved reading and synthesizing a lot of seemingly unrelated literature (i.e. machine learning, computer vision) to pick the best technique for my case. Some methods that *didn't* make the cut include: "Let's make all of the images black and white!" and "aslsfalsjfsldjf"

Preliminary tests showed that just small differences in spectral signature used to "train" the classifier led to very large differences in classified image output.


different spectral signatures used to "train" the classifier led to very high variation between supervised classification results for the same image. To counteract this variation, I took a **"Monte-Carlo-ish"** approach: **classify each photograph 1000 times** based on a random subset of training spectra, and create a final land cover classification based on the average of these 1000 runs.

To try and control for the effect of image artifacts on classification accuracy, I classified a separate control site (CS) in each of our respective images 1000 times, using the same 1000 signature files on which our HSL classifications were based. 

We assumed that the true bare area at CS was not changing over time and assumed that the mean of the 23 bare area estimates represented this “true” bare area. By comparing how much the classified BA for that image differed from the “true” CS amount, we calculated a positive or negative percent difference which could be attributed to image artifacts. We then adjusted each of our HSL BA estimates by this percent difference, which increased or decreased the estimate to compensate for under- or over-estimation of bare ground, respectively.

{% include elements/figure.html image="/myassets/HSL_slide15_change.jpg" caption="Four years of historical photographs and their average land cover classification within the region of interest (orange), about 31.6 hectares." %}


### Outcome Highlights ###

* Between 1951 and 1987, canopy cover at Horseshoe Lake remained relatively constant, with bare ground area beginning to increase in 1992. 
* Though field observations seemed to indicate that dieoff had stabilized by 2005, our results show more fluctuation in treeless area than expected after that date---possibly due to significant plant regrowth and large windstorms causing tree fall. 
* Despite subsequent spikes in CO2 flux in the region, the footprint/extent of tree kill remained stable from 2001-2014.



* Gained extensive practice in manual georectification of historical images and technical familiarity with various warps used when georectifying
* Sourced historical photographs from EROS EarthExplorer and the Map & Imagery Laboratory at UC Santa Barbara, and added XX new images to the project's imagery timeline.
* Improved the classification accuracy from previous summer's work 
* Worked very independently with regular status updates to supervisor. 


Sources cited on this page:  
Cook et al 2001
Lewicki et al 2014
(Werner et al, 2014) 



<< [Back to Projects](/projects/)