# Lidar Openness Index
<img src="https://www.ace-eco.org/vol17/iss1/art16/figure1.png" width="100%" title="https://www.ace-eco.org/vol17/iss1/art16/figure1.png">
This repository contains all code and data needed to reproduce the analyses reported in ["A lidar-based openness index to aid conservation planning for grassland wildlife" (Allen et al. 2022).](https://doi.org/10.5751/ACE-02078-170116) (doi: 10.5751/ACE-02078-170116). The archived repository used in the paper also lives [here on OSF](https://doi.org/10.17605/OSF.IO/VG5HU).

Potentially useful things in here: 1) instructions on how to calculate the openness index; 2) an example of using Restricted Spatial Regression (RSR) to fit an occupancy model in the presence of (lots of) spatial autocorrelation.

## Contents
The two .rmd files contain the R code for creating and manipulating the openness index (openness_mapping.rmd) and performing the occupancy modeling (openness_occupancy_modeling.rmd).

The data folder contains:

- the Duke Farms Kaufman/Skeet Shoot field and treeline shapefiles required for some analyses

- a template raster used for reprojection

- the horizon raster outputs from GRASS in the "horizon_rasters" folder (i.e., calculated mean and max angle to the horizon from each cell for each scenario - baseline, no powerlines, no treelines, no SW treeline, etc). 

- the 9 lidar point cloud files in the "lidar2018" folder. These "Northwest New Jersey 2018" lidar tiles can also be downloaded here: https://njgin.nj.gov/njgin/edata/elevation/index.html#!/

- the grsp.occupancy.openness.csv file, which contains all bird and covariate data needed to conduct the occupancy analysis. Descriptions of the fields in that file are as follows:

pt: survey point unique ID
site: Kaufman ("K") or Skeet Shoot ("S") field
latitude: decimal degrees (WGS84)	
longitude: decimal degrees (WGS84)
occ1-occ4: detection/non-detection measurements in survey periods 1-4	
obs1-obs4: observer for each point during survey periods 1-4	
ord1-ord4: ordinal date (1-365) of each point survey in periods 1-4
dtime1-dtime4: time of day (hour and decimal minutes) of each point survey in periods 1-4
mean2018: mean-angle openness measure at each point
max2018: max-angle openness measure at each point
No_trees_mean: mean-angle openness measure at each point based on raster with no treelines
No_trees_max: max-angle openness measure at each point based on raster with no treelines
No_wires_mean: mean-angle openness measure at each point based on raster with no powerlines
No_wires_max: mean-angle openness measure at each point based on raster with no powerlines
No_SW_mean: mean-angle openness measure at each point based on raster with no SW treeline
No_SW_max: max-angle openness measure at each point based on raster with no SW treeline
No_SE_mean: mean-angle openness measure at each point based on raster with no SE treeline
No_SE_max: max-angle openness measure at each point based on raster with no SE treeline
No_N_mean: mean-angle openness measure at each point based on raster with no N treeline
No_N_max: max-angle openness measure at each point based on raster with no N treeline

