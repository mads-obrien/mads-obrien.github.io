---
name: Yale MESc thesis
tools: [arcgis, data analysis, python, r, uav]
image: /myassets/thumbnail_uav_thesis.jpg
description: Did the big scary thing! With drones
---

## Master of Environmental Science Thesis ##
#### *"UAV deployment for fine-scale CO2 estimation in a mid-size city"* 

{% capture carousel_images %}
/myassets/20191014_143542.jpg
/myassets/20191014_152754.jpg
{% endcapture %}
{% include elements/carousel.html %}

{% include elements/button.html link="/pages/404.html" text="Full Manuscript PDF" style="primary" size="sm" %}
{% include elements/button.html link="/myassets/AGU2019_36x60_MAO_v4.pdf" text="View Conference Poster" style="primary" size="sm" %}

*Duration:* March 2019 - August 2020  
*Affiliation:* Yale School of the Environment  
*My Role:* The one and only grad student...  

### The Task:

My PI Dr. Natalie Schultz received a grant from the Connecticut Space Grant Consortium, to pilot (no pun intended) a new method for estimating CO2 flux in cities via a sensor-laden UAV platform. I collaborated with her as her first research assistant on the grant. 

### My Approach:

We did a lot of things. A lot of this phase being platform development and testing…. More robust field flight campaigns are a step for later.
We experimented with instrument placement, to find ideal spot for mounting the sensors on the UAV to avoid the effect of rotor wind. 

### Outcome highlights
* Based on our literature review, we also calibrated our small, cheap CO2 sensor against a high accuracy one using multiple regression. Wrote a script to convert our “raw” CO2 measurements in the field to the “corrected” ones, based on the parameters (constants) from the regression. CODE SNIPPET?  

```r
install.packages("data.table")

#Load data to be corrected 
#Must contain: raw CO2 values, temperature, pressure, and humidity
tocorr <- fread("U:/path/to/DataToCorrect.csv")

#Load calibration data (the basis for correcting K30 values)
#Must contain: CO2 values from LGR, CO2 values from a collocated K-30, temp, pressure, and humid from a collocated biomet sensor
calibdat <- fread("U:/path/to/FullCalibrationDataset.csv")

#Use a regression to obtain the coefficients which describe how the raw K30 values relate to the LGR's "true" CO2 values
#Replace vars within `lm()` with var names from calibration dataset
model <- lm(CO2_ppm ~ ReferenceCO2ppm + Pressure + AirTemp + Humidity, data=calibdat)

#OPTIONAL: View residual plots to assess quality of the regression

#Correct the raw K30 values
#assign aliases to variables to be used in correction equation below
k30raw <- tocorr$CO2ppm
p <- tocorr$iMetPressure
t <- tocorr$iMetAirTemp
q <- tocorr$mixrat

#Construct a new field containing **corrected** K30 values!
paste("K30 value correction using equation",model_eqn)
tocorr$k30_corr<- (k30raw - model$coefficients[1] -  (model$coefficients[3]*p) - 
                        (model$coefficients[4]*t) - (model$coefficients[5]*q)) / model$coefficients[2]

# calculate difference between original and corrected K30 values, save result to new field
tocorr$k30_corr_diff <- k30raw - tocorr$k30_corr

```

<< [Back to Projects](/projects/)