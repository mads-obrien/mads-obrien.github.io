---
name: ArcFootprint
tools: [arcgis, python]
image: /myassets/thumbnail_arcfootprint.jpg
description: A custom-built ArcToolbox tool for estimating gas flux footprints directly within ArcMap.
---

## ArcFootprint, an ArcTool for Flux Footprint Estimation ##
#### *An ArcTool for Flux Footprint Estimation* 

![A photo](http://placekitten.com/400/375)

{% include elements/button.html link="/myassets/OBrien,Mads_FinalProject_ArcFootprint.pdf" text="Full Report PDF" style="primary" size="sm" %}
{% include elements/button.html link="/myassets/ArcFootprint.zip" text="Download toolbox .zip" style="primary" size="sm" %}

*Duration:* Oct 2019 - Dec 2019  
*Affiliation:* Yale School of Environment  
*What:* Open-source tool  
*My Role:* Sole analyst and report author

### The Task:

In [Dana Tomlin](https://en.wikipedia.org/wiki/Dana_Tomlin)'s *Geospatial Software Design* course, my term project was to program an ArcToolbox tool, a GUI that would be easy for others to use. 

In my previous work, I’d seen flux footprints calculated by my colleagues using the software that comes with the trace gas sensors and flux towers. Lots of software exists to calculate gas flux footprints, but they require standalone software or require advanced programming skills. (Sometimes doesn't play nicely with ArcMap, doesn't directly import. And multi-step conversions increase the lag time between footprint calculation and comparing footprint extent with other spatial datasets.)


### Project Goals:
I wanted to create an easy to use GUI that allows anyone to easily calculate a flux footprint estimate within ArcGIS, where they can input data they’ve collected on their own to just to visualize others’ flux data for mapping purposes.

* Build a user-friendly, point-and-click ArcToolbox tool for generating spatial extents of flux footprints (as shapefiles), based upon meteorological variables collected from gas sensors.
* Construct separate polygons for each source area (50%, 90%, etc.), making it easy for the user to run subsequent Zonal Statistics within each zone.
* Create a tool that will not only benefit my own academic research, but hopefully benefit others conducting meteorological research as well.  

![A photo](/myassets/fluxfootprintdialogbox.jpg)

### Outcome highlights:  
The code is broken down into two parts: The `FFP()` function constructed by [Kljun et al (2015)](https://gmd.copernicus.org/articles/8/3695/2015/), and then some add-on code that allows those ellipses to be drawn as shapefiles rather than simply plotted in a Python window. Some features I've added, specifically for ArcMap, include:  

* A snippet of code **alters the drawing order of the ellipses**, so that the smallest flux area always appears on top. This allows for easier symbology when making maps from the flux footprints.

```python
arcpy.CalculateField_management(polygons, "footptAREA", "float(!SHAPE.area!)", "PYTHON")
arcpy.Sort_management(polygons, polygonsSorted, [["footptAREA", "DESCENDING"]])
```

* **Linear units are automatically converted, if necessary**. The tool detects whether the linear unit used by the input sensor location’s projection is Feet or Meters. The output ellipses use the same projection as the input sensor location. If input point CRS uses meters, aka  `if spatial_ref.metersPerUnit == 1.0:`, proceed with arithmetic. If not...

```python
else:
	# save a factor to convert other-units to meters
	conversion = float(spatial_ref.metersPerUnit) 
	for boundary in xrs: # for each requested footprint outline...
		boundxlist = []
		for vertex in boundary: # for each vertex in a given footprint outline...
			newx = originx + (vertex / conversion) # returns number as Double
			boundxlist.append(newx) # append translated X-value to list
		newxshapes.append(boundxlist)

# repeat for y coordinates
```


* A **drop-down menu** in the GUI for the user to select the **season, a proxy for atmospheric boundary layer height**. Since the height of the boundary layer can change dramatically throughout the year, but knowing what value to put in for the boundary layer may be a lot to ask the user, I provided a simple dictionary that inserts a suitable estimate for BLH based on observation season.  

```python
#look up average values of boundary layer height
seasondictionary = {"Summer (June, July, Aug)": 1000,
		"Fall (Sept, Oct, Nov)": 600,
		"Winter (Dec, Jan, Feb)": 300,
		"Spring (March, April, May)": 1200,
		"Unknown":775} 

#returns the boundary layer height value as a number
PBLH = float(seasondictionary[season])
```  


<< [Back to Projects](/projects/)