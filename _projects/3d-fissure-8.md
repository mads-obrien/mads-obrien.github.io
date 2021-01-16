---
name: Photogrammetry of Fissure 8, Kiauea
tools: [agisoft photoscan, data analysis, remote sensing, uav, yale]
image: /myassets/thumbnail_fissure_8.jpg
description: Using 3D models of a volcanic fissure based on drone images of fissure structure from the 2018 Kilauea eruption to describe changes in its morphology.
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
*Affiliation:* Yale School of Environment
*What:* Course project
*My Role:* Sole analyst and author


For my *Photogrammetry with Drones* course project, I reached out to contacts at the US Geological Survey to ask if any of their imagery would be available for a project. Thanks to Angie Diefenbach with USGS / VDAP, I gained access to then-unreleased UAV imagery of the Lower East Rift Zone of Mount Kilauea, Hawai’i. After decades of dormancy, Kilauea actively erupting on May 3, 2018. Fissure #8, which appeared in a populous subdivision, was the most active and most closely observed fissure during this eruption phase. 


### The Objective: CLIENT EXPECTATIONS

* Create a 3D mesh and digital elevation model (DEM) of Fissure 8's spatter cone and lava channel from two drone photo surveys, taken 7 days apart
* Georeference one of the 3D models, which lacked GPS coordinates
* Calculate the difference in fissure volume between the two dates
* Assess the height and terrain of the F8 cone in the UAV-derived models, relative to a LIDAR-derived surface measured earlier in Summer 2018
* Create cross-sections of the fissure structure and compare across dates

### The Solution:

Cross section lines were drawn in ArcMap across regions of potential surface change suggested by the analyses above. Elevation profiles were generated for each line using the Stack Profile 3D Analyst tool in ArcMap, and profiles for July, August, and September were plotted simultaneously.

I created a 3D mesh / DEM of the fissure using AgiSoft Photoscan. Needed to do a lot of editing of the point cloud to remove points caused by steam. (Screenshot maybe)

Only one of the UAV flights had active GPS, so I used the images and DEM of the Aug flight to georeferenced the Sept flight within AgiSoft.
Since Photoscan’s “volume calculation” / cut fill tool didn’t have a ground plane beneath it, I exported the DEM to ArcScene 10.7 to calculate the volume of the difference there. 
Wanted to compare the volume differences to LIDAR, collected by USGS and UH Hilo, from July. Great discrepancy between the elevations of the LIDAR and the 3D models – however, the offset I found matched the offset that HVO was seeing. 


Cross section lines were drawn in ArcMap across regions of potential surface change suggested by the analyses above. Elevation profiles were generated for each line using the Stack Profile 3D Analyst tool in ArcMap, and profiles for July, August, and September were plotted simultaneously.

### Outcome highlights
* Lava lake appeared sometime between Aug 27 and Sept 2 amounting to 13,066.114197 m3 (+/- 28.09 m3). Under the assumption of lava infill starting on Sept 1, estimated rate of lava fill is 363 m3 per hour.
* Two zones of significant channel shallowing developed between July and Aug 27, likely due to pooling slow-moving lava hardening into basalt rock.
* The area of the crater floor as of Sept 1 matches the size of the crater floor in our Aug 27 flight almost exactly, affirming that UAV imagery flown with these parameters are effective for producing useful models for earth scientists.

Data source:  
Patrick, M.R., Dietterich, H., Lyons, J., Diefenbach, A., Parcheta, C., Anderson, K., Namiki, A., Sumita, I., Shiro, B., and Kauahikaua, J., 2019, Cyclic lava effusion during the 2018 eruption of Kīlauea Volcano: data release: U.S. Geological Survey data release, https://doi.org/10.5066/P9PJZ17R.


<< [Back to Projects](/projects/)