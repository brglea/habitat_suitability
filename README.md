# Habitat Suitability - Case Study on Sorghastrum Nutans


## Project Description
Create a habitat suitability model for Sorghastrum nutans, a grass native to North America. This habitat suitability model will focus on creating a modular, reproducible workflow. In the past 50 years, its range has moved northward. The model will be based on combining multiple data layers related to soil, topography, and climate.

Two climate models are chosen:

Two variables related to soil are chosen:


## Steps on project
1. Define your study area: Download the USFS National Grassland Units and select your study site(s).**Choose AT LEAST 2!**
    a. Study areas chosen:

2. Fit a model: For each grassland:
    a. Download model variables as raster layers covering your study area envelope, including:
        i. At least one soil variable from the POLARIS dataset
        ii. Elevation from the SRTM (available from the APPEEARS API)
        iii. At least one climate variable from the MACAv2 dataset, accessible from Climate Toolbox. 
        *Graduate students should download at least two)

    b. Calculate at least one derived topographic** variable** (slope or aspect) to use in your model. Use the xarray-spatial library, which is available in the latest earth-analytics-python environment (but will need to be installed/updated if you are working on your own machine). Note that calculated slope may not be correct if you are using a CRS with units of degrees; you should re-project into a projected coordinate system with units of meters, such as the appropriate UTM Zone.

    c. Harmonize your data - make sure that the grids for each of your layers match up. Check out the ds.rio.reproject_match() method from rioxarray.
    
    d. Build your model. You can use any model you wish, so long as you explain your choice. However, if you are not sure what to do, we recommend building a fuzzy logic model (see below).

3. Present your results in at least one figure for each grassland/climate scenario combination.


DOI :