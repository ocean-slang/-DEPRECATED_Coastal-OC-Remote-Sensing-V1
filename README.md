# Modeling Coastal Water Clarity Using Landsat-8 and Sentinel-2 version 1
# Please see version 2 for most recent data and code

Tools and resources for ocean color remote sensing of the Virginia Coast Reserve. Can be modified for your water body of interest. Folder contains code for analysis and modeling, resources, code for processing Level-1 Landsat-8/Sentinel-2 images, etc. 

**Overview of workflow:**
1. Download Level-1 Landsat-8 (Collection 1) and Sentinel-2 (bulk download tools available, see below)

2. Process with l2gen in NASA SeaDAS or REMSEM ACOLITE to get Level-2 images (use l2genbash or GUI) - please see: https://github.com/ocean-slang/SeaDAS

3. **algosMatlab** Use Level-2 NetCDF images as inputs to MATLAB code. Code extracts data from images and implements ocean color algorithms (eg. Secchi disk depth, Zsd). 

3a. Optional: **lmnonlinear** Modify Lee et al. 2016 Secchi depth algorithm (https://doi.org/10.1016/j.rse.2016.02.033) using Levenburg-Marquardt algorithm (adjusts free parameters of equation, alternative method instead of linear model)

4. **modeling_and_analysis** R code for modeling and data analysis available. Empirical (linear) fit used to improve satellite Secchi depth estimates. Data for Virginia Coast Reserve included as .csv's

**Bulk download tools:**

getOC (not available for Landsat-8) https://github.com/OceanOptics/getOC/tree/features/module

Batch download tool for Landsat-8 from USGS: https://dds.cr.usgs.gov/bulk


**Credits:**
bash code for l2gen written by Sarah Lang, with help from NASA OC forum
https://oceancolor.gsfc.nasa.gov/forum/oceancolor/topic_show.pl?tid=8666 
https://oceancolor.gsfc.nasa.gov/forum/oceancolor/topic_show.pl?tid=8810 
https://oceancolor.gsfc.nasa.gov/forum/oceancolor/topic_show.pl?tid=8654 

MATLAB code written by Kelly Luis, modified by Sarah Lang

you can find more MATLAB code for processing and analysis at Kelly's github: https://github.com/m11keluis/oceanoptics

R code written by Sarah Lang

If you have questions, feel free to email me at slang@uri.edu
If you would be interested in a video tutorial for this procedure, please let me know!

Lang‡, S.E., K.M.A. Luis, S.C. Doney, and M.C.N. Castorani. Modeling coastal water clarity using Landsat-8 and Sentinel-2. In review.
