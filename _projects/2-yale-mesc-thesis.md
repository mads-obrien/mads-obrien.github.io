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


{% include elements/button.html link="/pages/404.html" text="Full Manuscript PDF [TBA]" style="primary" size="sm" %}
{% include elements/button.html link="/myassets/AGU2019_36x60_MAO_v4.pdf" text="View Conference Poster" style="primary" size="sm" %}

**Duration:** March 2019 - August 2020  
**Affiliation:** Yale School of the Environment  
**What:** Master of Environmental Science thesis  
**My Role:** Primary researcher and thesis author

### The Task:

Urban areas and the utilities that serve them generate up to 80% of anthropogenic carbon dioxide (CO2) emissions worldwide [(Satterthwaite, 2008)](https://doi.org/10.1177/0956247808096127). When we can quantify where, and how much, carbon dioxide is being emitted *within* a city, local emission reduction targets can become more actionable. However, it's difficult to estimate intra-city carbon flux using existing atmospheric science methods.

In collaboration with Dr. Natalie Schultz at Yale's [Center for Earth Observation](https://yceo.yale.edu/), we sought to build and test a new method for estimating CO2 flux in cities: load a UAV with lightweight, low-cost sensors and fly it in the region of interest. I served as her first funded research assistant on her Connecticut Space Grant Consortium award.

I primarily contributed to the platform development and testing phase of this project. I read and experimented extensively to identify the ideal spots for mounting sensors on the UAV, to prevent rotor wind from affecting measurements. I also designed numerous indoor and outdoor experiments to test how our instrumentation would perform under various conditions (i.e., hot weather, strong wind, high altitudes, etc.). Lastly, I led a handful of small data collection deployments around the city of New Haven, and I suggested plans for more robust flight campaigns for the future.


### Outcome highlights
By using a multivariate regression [(Martin et al, 2017)](https://doi.org/10.5194/amt-10-2383-2017) to calibrate our mobile, low-cost CO2 sensor against a high-precision CO2 and meteorological instrument, we were able to **improve upon the sensor manufacturer’s accuracy by ~80%.** 

- Wrote a script to convert our “raw” CO2 measurements from the field to the “corrected” ones, based on variable relationships we could quantify in the lab (such as ambient temperature's effect on the recorded CO2 concentration). 
- Used a Raspberry Pi script to record observations from small sensors connected via serial port. I continued to revise the initial script as the project progressed as our instrumentation and needs changed.
- Conducted extensive data cleaning and analysis in R.
- Safely planned and conducted UAV flights in populated areas as a licensed drone pilot, adhering to all local and federal regulations.


<< [Back to Projects](/projects/)