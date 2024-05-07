---
name: Final Website
tools: [Python, HTML, vega-lite]
image: assets/pngs/cars.png
description: This is a test to see if it works
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---

# writeup
We used geopandas to create a geographical plot of the earthquake events. You can see the earthquakes on the map, they are color coded by the magnitude and sized by depth. Users can use this visualization to gain insights into earthquake occurrences and their spatial distribution such as identifying high seismic regions. The patterns can be analyzed to see if there is correlation between earthquakes’ magnitude, depth, and geographic locations. Users can assess the impacts of recent earthquakes, which can help with disaster preparedness and responses. 

<iframe src="{{ site.baseurl }}/assets/output.html" style="width: 100%; height: 500px;"></iframe>


# writeup
Here we included an interactive map visualization that allows users to explore the earthquake data by selecting specific magnitude types and ranges, then providing you with a dynamic way to analyze seismic events on a map. The dropdown menu included allows you to select different magnitude types to filter earthquakes based on the measurement method used. Additionally, by moving the magnitude slider, users can set a minimum magnitude for earthquakes to be displayed on the map. Also, the markers on the map allow users to zoom in and out and pan across different regions. By clicking on each individual marker, you can see information about each earthquake including: magnitude, magnitude type, depth, and location. 
Try experimenting with different magitue type and magnitude threshold combinations. This will allow you to compare how earthquake data changes under different scenarios. We hope this helps you gain insights into the relationship between earthquakes. 



<iframe src="{{ site.baseurl }}/assets/earthquake_map.html" style="width: 100%; height: 500px;"></iframe>







