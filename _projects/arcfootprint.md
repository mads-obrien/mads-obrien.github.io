---
name: ArcFootprint
tools: [arcgis, python]
image: /myassets/thumbnail_arcfootprint.jpg
description: A custom-built ArcToolbox tool for estimating gas flux footprints directly within ArcMap.
---

## ArcFootprint, an ArcTool for Flux Footprint Estimation ##

![A photo](http://placekitten.com/400/375)

{% include elements/button.html link="/myassets/OBrien,Mads_FinalProject_ArcFootprint.pdf" text="Full Report PDF" style="primary" size="sm" %}
{% include elements/button.html link="/myassets/ArcFootprint.zip" text="Download toolbox .zip" style="primary" size="sm" %}

*Duration:* Oct 2019 - Dec 2019  
*Affiliation:* Yale School of Environment  
*What:* Open-source tool
*My Role:* Sole analyst and report author

### The Task:

In Dana Tomlin’s Geospatial Software Design course, my term project was to program an ArcToolbox tool, a GUI that would be easy for others to use. In my previous work, I’d seen flux footprints calculated by my colleagues using the software that comes with the trace gas sensors and flux towers. I wanted to create an easy to use GUI that allows anyone to easily calculate a flux footprint estimate within ArcGIS, where they can input data they’ve collected on their own to just to visualize others’ flux data for mapping purposes.


### Outcome highlights:  
The code is broken down into two parts: The Kljun et al Python script for generating flux footprints, and then some add-on code that allows those ellipses to be drawn as shapefiles rather than simply plotted in a Python window. 

Some features of the tool include:  

* A snippet of code **alters the drawing order of the ellipses**, so that the smallest area always appears on top. This allows for easier symbology when making maps from the flux footprints. SORT THE FEATURES FROM LARGEST TO SMALLEST (based on area), so smaller footprints draw on top of larger ones! (90, 70, etc)  

```python
arcpy.CalculateField_management(mergedpolys, "footptAREA", "float(!SHAPE.area!)", "PYTHON")

arcpy.Sort_management(mergedpolys, mergedsorted, [["footptAREA", "DESCENDING"]])
```

* **Auto-handling of linear unit conversions**. The tool detects whether the linear unit used by the input sensor location’s projection is Feet or Meters. The output ellipses use the same projection as the input sensor location. If input point CRS uses meters, aka  `if spatial_ref.metersPerUnit == 1.0:`, proceed with arithmetic.

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