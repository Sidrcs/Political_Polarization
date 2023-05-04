# Measuring and analyzing political polarization in the UK using Geopandas and PySAL.
<a href = "https://sidrcs.github.io/maps/index.html"> Chinna Subbaraya Siddharth Ramavajjala <sup>a</sup></a>, <a href = ""> Ramakrishna Raju Gangaraju  <sup>a</sup></a> <br> a - Department of Geography, University of Wisconsin - Madison
<br>
<h3><b>Motivation and Topic of Interest:</h3></b>
<p>Political polarization is often considered a critical parameter for the stability of a government, social tensions (Esteban et al., 2012), policy uncertainty (Funke et al., 2016), economic fluctuations, and low economic growth. However, quantifying political polarization is challenging and complicated as it depends on several factors like income, level of education, age of the population, variability of job status (percentage of employed), and a fraction of employed. Therefore, it computes categorical data encoded into values, giving a scale. Interestingly, most of the research is carried out in the United States, and the application of measurement polarization is not a common sight across developed economies despite the enormous power of data they hold.</p>

<h3><b>Data:</b></h3>
<ul>
<li>British Household Panel Survey (BHPS) data:  - https://beta.ukdataservice.ac.uk/datacatalogue/studies/study?id=5151#!/access-data</li>
<li>UK Shapefiles - https://geoportal.statistics.gov.uk/datasets/ons::nuts1-jan-2018-super-generalised-clipped-boundaries-in-the-uk/explore?location=49.270533%2C12.096034%2C5.65</li>
</ul>

<h3><b>Spatial Bigdata Visualization Flowchart:</b></h3>

<img src = "https://github.com/Sidrcs/Political_Polarization/blob/main/images/flow.drawio.png?raw=true">

<h3><b>Methods:</b></h3>
<ul>
<p>As part of the project, we will implement methods and techniques used in analyzing BHPS titled "Political polarization in the UK: measures and socioeconomic correlates” by Daryna Grechyna (2022). Therefore, the project uses raw data, consisting of several folders in SPSS format, which would be read in pandas. Indirect calculations are performed based on variables of interest.
The evaluation of political polarization will be performed on the following statements, which are available in BHPS data.
<p>
<br>
<ul><li>Statement 1 (S1): “Private enterprise is the best way to solve Britain’s economic problems.”</li>
<li>Statement 2 (S2): “Major public services and industries ought to be in state ownership.”</li>
<li>Statement 3 (S3): “It is the government’s responsibility to provide a job for everyone who wants one.”</li></ul>
<br>
<p>The political polarization measures implemented are:<p>
<ul> <li> Lindqvist and Ostling (2010)</li>
<li> Duca and Saving (2016)</li>
<li> Abramowitz and Saunders (2008)</li> </ul>
<br>
<p>The extracted and analyzed data would then be combined with Geopandas and PySAL libraries to calculate hotspots and cold spots of polarization in the UK.</p>

<h3><b>Results:</b></h3>
  
<img src = "https://github.com/Sidrcs/Political_Polarization/blob/main/images/LISA_Frac_Employed_Temporal.gif?raw=true" align = "center"> 
<p align = "center">Local Moran's I of <b>Fraction of Employed</b> in the years 1995, 2000 and 2004</p>
  
<img src = "https://github.com/Sidrcs/Political_Polarization/blob/main/images/Temporal_Correlations.gif?raw=true">
<p align = "center"><b> Correlation matrices</b> between variables and political polarization measurements in the years 1995, 2000 and 2004</p>

<img src = "https://github.com/Sidrcs/Political_Polarization/blob/main/images/Temporal_S3_Opinions_byRegion.gif?raw=true">
<p align = "center"><b>Opinion change for Statement 3</b> by each region in the years 1995, 2000 and 2004</p>

<img src = "https://github.com/Sidrcs/Political_Polarization/blob/main/images/Temporal_Distributions.gif?raw=true">
<p align = "center"><b>Opinion distribution change for all Statements</b> in the years 1995, 2000 and 2004</p>



