# Final-Project

This is my final project for MAP 671.

Project Title: Lava Flow Hazard Of Hawaii

Collaborator: Instructor GitHub username jfobrycki

# Background

For this project, I will be creating a final map that uses the map of Hawaii. The Big Island will be the main focus of this project. This map will focus on the volcano lava flow hazard locations which will involve the roads in the area. It would showcase which area has the most hazard and how it would affect the roads.

# How To Create The Map
These are the instructions on how this map was created:

![map](crs_projection.png)

Change the assigned CRS Projection to ESRI:102007. 

![map](filter_hawaii.png)

Right click the cb_2022_us_state_500k source. Click on the filter section, and then select "Name". Click the equal sign, and then click on the sample button. Once done, select "Hawaii". It will produce something like "NAME" = "Hawaii".

![map](QuickOSM.png)

Afterwards, use the QuickOSM to create features. To access the QuickOSM tool, click on the Vector section. After clicking on the QuickOSM tool, click on "quick query".  In this case, "Highways/Streets" was used. After selecting the tools to generate, change it to "Canvas Extent". Then, click "Run Query" and it will then appear on the layers section and the map itself.

![map](export_layers.png)
Export the layers when it is ready to do so. Save as GeoPackage, and change the CRS to ESRI:102007.

The source that is also used will be the Hawaii Geoportal. To access the link, click here: https://geoportal.hawaii.gov/

Let's say I want to find information about lava. Select hazards, and then download the maps, and select the following: Volcano Lava Flow Hazard Zones (Buffer), Volcano Lava Flow Hazard Zones, and Volcano Lava Flow Hazard Zones (Line). Download as a GeoJSON file. You can click on this link to find the three maps in a easier fashion: https://geoportal.hawaii.gov/datasets/HiStateGIS::volcano-lava-flow-hazard-zones/explore

![map](Join_attributes_by_location_summary.png)
Next up, a joined layer will be created. To do that, select "Join attributes by layer (summary)". It will produce something like this (see above). Once clicked, it will produce something like this. In "join to features in", select the 2020_Census_Tracts file, which is a ESRI:102007 projection. In "by comparing to", select the volcano_lava_flow_hazard_zones file, which is also a ESRI:102007 projection. The joined layer will be saved as a "geopackage", and then, click run.


On the joined layer, select Properties. Go to the Symbology section and add vhzones_id to the value section. Then, change the feature to "Addition". After that, select the color ramp and enter whichever gradient color works. The mode is on Equal Count (Quantile). Then, when ready, click "classify". It should give a gradient color pattern.

# Conclusion
Based on the map, the area with the most lava hazard is