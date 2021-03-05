---
name: Yale MESc thesis
tools: [trace gases, python, r, uav]
image: /myassets/thumbnail_uav_thesis.jpg
description: A pilot study (no pun intended) of an airborne instrument for estimating carbon dioxide flux in cities. 
---

## Master of Environmental Science Thesis ##
#### *"UAV deployment for fine-scale CO2 estimation in a mid-size city"* 


{% capture carousel_images %}
/myassets/20191014_143542.jpg
/myassets/20191014_152754.jpg
/myassets/20190523_152555.jpg
{% endcapture %}

{% capture carousel_captions %}
UAV platform, with biomet sensors mounted
Test flight of sensing platform
Calibrating mobile sensors against a research-grade CO2 sensor
{% endcapture %}

{% include elements/carousel.html %}


**Duration:** March 2019 - August 2020  
**Affiliation:** Yale School of the Environment  
**What:** Master of Environmental Science thesis  
**My Role:** Almost everything

{% include elements/button.html link="/pages/404.html" text="Full Manuscript PDF [TBA]" style="primary" size="sm" %}
{% include elements/button.html link="/myassets/AGU2019_36x60_MAO_v4.pdf" text="View Conference Poster" style="primary" size="sm" %}


### The Task:

Urban areas and the utilities that serve them generate up to 80% of anthropogenic carbon dioxide (CO2) emissions worldwide [cite]. When we can quantify where, and how much, carbon dioxide is being emitted *within* a city, local emission reduction targets can become more actionable.
However, it's difficult to estimate carbon flux at such a fine scale using existing atmospheric science methods. 

My unofficial thesis PI, Dr. Natalie Schultz, received funding from the Connecticut Space Grant Consortium to build and test a new method for estimating CO2 flux in cities: load a UAV with lightweight, low-cost sensors and fly it in the region of interest. I collaborated with her as the first research assistant on the grant. 


A large percentage of my contribution to this project was the platform development and testing phase, with more robust field flight campaigns to follow. We read and experimented extensively regarding instrument placement, to find the ideal spots for mounting sensors on the UAV to avoid the effect of rotor wind. I also designed numerous small-scale experiments to test how our instrumentation would perform under various conditions (i.e., hot weather, strong wind, high altitudes, etc.).



### Outcome highlights
* Using a multivariate regression to calibrate our mobile, low-cost CO2 sensor against a high-precision CO2 and meteorological instrument, we were able to improve upon the manufacturer’s accuracy of the low-cost sensor readings by ~80%. 
* Wrote a script to convert our “raw” CO2 measurements from the field to the “corrected” ones, based on variable relationships we could quantify in the lab (such as ambient temperature's effect on the recorded CO2 concentration).
* Used Raspberry Pi script to record observations from small sensors connected via serial port. I revised the initial script (written by another graduate student) as the project progressed, to make sure it kept meeting our needs.
* Conducted extensive data cleaning and analysis in R.
* Safely planned and conducted UAV flights in populated areas, adhering to all local and federal regulations.



<< [Back to Projects](/projects/)