---
name: Photogrammetry of Fissure 8, Kiauea
tools: [agisoft photoscan, data analysis, remote sensing, uav, yale]
image: /myassets/thumbnail_fissure_8.jpg
description: I built a 3D model of a volcanic fissure from drone images during the 2018 Kilauea eruption, to describe changes in the fissure's morphology.
---

## Photogrammetry of Fissure 8, Kiauea ##
#### *"Estimating Volume Changes in Volcanic Features with UAV Photogrammetry"*

{% capture carousel_images %}
https://bit.ly/2BBbVhc
https://bit.ly/2DOtxXB
{% endcapture %}
{% include elements/carousel.html %}

{% include elements/button.html link="/myassets/OBrienMadeleine_Drones_FinalReport_1-14-19.pdf" text="Full Report PDF" style="primary" size="sm" %}

*Duration:* Oct 2018 - Dec 2018  
*Affiliation:* Yale School of the Environment  
*What:* Course project  
*My Role:* Sole analyst and author


After decades of dormancy, Mount Kilauea began actively erupting on May 3, 2018. Fissure #8, which appeared in a populous subdivision, was the most active and most closely observed fissure during this eruption phase. 

For my *Photogrammetry with Drones* course project, I worked with then-unreleased UAV imagery of the Lower East Rift Zone of Mount Kilauea, Hawai’i (thanks to [Angie Diefenbach]( https://www.usgs.gov/staff-profiles/angie-diefenbach), USGS / VDAP) to try to reproduce the findings of USGS analysts.

### The Objectives:

* Create a 3D mesh and digital elevation model (DEM) of Fissure 8's spatter cone and lava channel based on two UAV photo surveys, taken 7 days apart (late August & early September)
* Georeference one of the 3D models, which lacked GPS coordinates
* Calculate the difference in fissure volume between the two dates
* Compare the height of the UAV-derived fissure models to a LIDAR-derived surface surveyed earlier that summer
* Visualize cross-sections of the fissure structure and compare across dates


### The Solution:

I created a 3D mesh / DEM of the fissure using AgiSoft Photoscan. The point cloud required extensive manual editing to remove points erroneous points caused by steam. 

I used the photographs and DEM of the August model to georeference the September model within AgiSoft.

Photoscan’s volume calculation tool failed to work for my purposes, since I didn’t have a reference plane upon which to place my spatter cone model. Instead, I exported my DEM to ArcScene 10.7 to calculate the volume difference between the August and September models. 

Finally, I plotted various cross-sections of the fissure with the Stack Profile 3D Analyst tool in ArcMap, to compare profiles of July, August, and September simultaneously.


### Outcome highlights
* The lava lake within the Fissure 8 cone appeared sometime between Aug 27 and Sept 2, containing an estimated 13,066 m^3 of lava (+/- 28 m^3). Assuming that lava infill began on Sept 1, according to field reports, the estimated rate of lava fill is 363 m^3 per hour.
* Big elevation discrepancies between the July LIDAR surface and the 3D models made the two impossible to compare quantitatively. However, the offset that I found matched the offset found by the Hawai’i Volcano Observatory. Plus, my cross-sections identified two zones of significant change between the LIDAR and my models much greater than expected horizontal errors; I identified them as areas of lava channel shallowing caused by slow-moving lava hardening into rock. 
* The area of the fissure crater floor in the August 3D model matches USGS field observations almost exactly (65 x 15 m). Meaning: this model is a good representation of the real thing, and provides a functionally useful model for earth scientists. 


Data source:  
Patrick, M.R., Dietterich, H., Lyons, J., Diefenbach, A., Parcheta, C., Anderson, K., Namiki, A., Sumita, I., Shiro, B., and Kauahikaua, J., 2019, Cyclic lava effusion during the 2018 eruption of Kīlauea Volcano: data release: U.S. Geological Survey data release, https://doi.org/10.5066/P9PJZ17R.


<< [Back to Projects](/projects/)