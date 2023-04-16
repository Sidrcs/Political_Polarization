# Devising a Python function to bind elevation from DEMs to Nodes and Edges in Open Street Maps (OSMnx).
<a href = "https://sidrcs.github.io/maps/index.html"> Chinna Subbaraya Siddharth Ramavajjala <sup>a</sup></a>, <a href = ""> Ramakrishna Raju Gangaraju  <sup>a</sup></a> <br> a - Department of Geography, University of Wisconsin - Madison
<br>
<h3>Motivation and Topic of Interest:</h3>
<p>Digital Elevation Model (DEM) is a widely used dataset for digital terrain analysis (DTA), flood mapping, and bike-ability & walkability analyses. On the other hand, Open Street Maps (OSM) is an extensively used geospatial data extraction source for road network analysis. Therefore, the crucial motivation for our project is to add elevation data to Nodes/Edges based on a DEM raster and create an export file that could be plugged into the modeling network in ArcGIS Pro.
<br>
Furthermore, several road networks in Wisconsin are deprived of elevation data. And it is crucial for modeling network datasets on and calculating route feasibility based on time. However, as part of the project, we wish to write a small Python function and compare the results against the OSMnx elevation function. For instance, counties like Door County do not have proper elevation data to their network datasets. Therefore, through this project, basic elevation information could be added to network datasets and analysis could be performed for walkability, bike-ability.</p>
<img src = "https://github.com/Sidrcs/Elevation_OSMnx/blob/main/images/RoadNetwork_NoElevation_Sid2023.png?raw=true"> 
<p align = "center"><i>1.1 Door County Road Network with No Elevation Information (From <a href = "https://geodata.wisc.edu/">GeoData@Wisconsin</a>)</i></p>
<img src = "https://github.com/Sidrcs/Elevation_OSMnx/blob/main/images/RoadNetwork_WithElevation_Sid2023.png?raw=true">
<p align = "center"><i>1.2 Brown County Road Network with Elevation Information (From <a href = "https://geodata.wisc.edu/">GeoData@Wisconsin</a>)</i></p>
<img src = "https://github.com/Sidrcs/Elevation_OSMnx/blob/main/images/RoadNetwork_NoElevation_NetworkDataset_Sid2023.png?raw=true">
<p align = "center"><i>1.3 Door County has no elevation and elevation model-based Network dataset cannot be created. (Screenshot from ArcGIS Pro)</i></p>
<h3>Data:</h3>
<ul>
<li>Elevation data (DEMs) of Wisconsin - https://geodata.wisc.edu/</li>
<li>OSMnx - https://osmnx.readthedocs.io/en/stable/</li>
<li>Strava - https://labs.strava.com/</li>
</ul>
<h3>Methods:</h3>
<ul><li>Currently, we planned to source inspiration from Jeff Boeing’s examples on elevation extraction from a raster and binding it to a network dataset containing Nodes/Edges - https://github.com/gboeing/osmnx-examples/blob/main/notebooks/12-node-elevations-edge-grades.ipynb</li>
<li> Also, we are analyzing different calculations and methods that could be applied from the paper titled “Modelling cyclists’ route choice using Strava and OSMnx: A case study of the City of Glasgow.” - https://www.sciencedirect.com/science/article/pii/S2590198221000051 </li>
<li>Based on feasibility, we might also add Strava API to analyze cycle routes to extract elevation data to understand bike-ability in Wisconsin.</li>
</ul>
<h3>Pseudo workflow:</h3>
<p>Import libraries --> Initialize elevation data and nodes/edges from OSMnx --> Extract elevation under each Node by using rasterio --> Use geopandas to bind the elevation data From Node – To Node and export them --> Perform statistical analysis of bike-ability using methods from mentioned paper* --> deploy Strava API and analyze bike routes to elevation information.</p>




