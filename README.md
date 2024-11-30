# Habitat Suitability - Case Study on Sorghastrum Nutans in Colorado

## DOI :

## Project Description
Create a habitat suitability model for 
[Sorghastrum nutans](https://plants.usda.gov/DocumentLibrary/plantguide/pdf/pg_sonu2.pdf), 
a grass native to North America. This habitat suitability model will focus on creating a 
modular, reproducible workflow. In the past 50 years, its range has moved northward. 
The model will be based on combining multiple data layers related to soil, topography, 
and climate.

Two variables related to soil are chosen:

Two climate models are chosen:


## Steps on project
1. Define study area: Download the 
[USFS National Grassland Units](https://data-usfs.hub.arcgis.com/datasets/usfs::national-grassland-units-feature-layer/explore?location=38.859474%2C-103.043221%2C6.81) 
and select your study site(s).**Choose AT LEAST 2!**
    a. Study areas chosen:
        i. *Comanche National Grassland*
        ii. *Pawnee National Grassland*

2. Fit a model: For each grassland:
    a. Download model variables as raster layers covering your study area envelope, including:
        i. Two soil variables from the POLARIS dataset
            A. 
            B.  
        ii. Elevation from the SRTM (available from the earthaccess API)
        iii. Two climate variables from the MACAv2 dataset, accessible from Climate Toolbox. 
            A. 
            B. 

    b. Calculate at least one derived topographic** variable** (slope or aspect) 
    to use in your model. Use the xarray-spatial library, which is available in 
    the latest earth-analytics-python environment (but will need to be 
    installed/updated if you are working on your own machine). Note that calculated 
    slope may not be correct if you are using a CRS with units of degrees; you 
    should re-project into a projected coordinate system with units of meters, 
    such as the appropriate UTM Zone.

    c. Harmonize your data - make sure that the grids for each of your layers 
    match up. Check out the ds.rio.reproject_match() method from rioxarray.
    
    d. Build a model. You can use any model you wish, so long as you explain 
    your choice. However, if you are not sure what to do, we recommend building 
    a fuzzy logic model (see below).
        i. Research S. nutans, and find out what optimal values are for each 
        variable you are using (e.g. soil pH, slope, and current climatological 
        annual precipitation).
        ii. For each digital number in each raster, assign a value from 0 to 1 
        for how close that grid square is to the optimum range (1=optimal, 0=incompatible).
        iii. Combine your layers by multiplying them together. This will give you a 
        single suitability number for each square. Check out this article about raster 
        math for more info.
        iii. Optionally, you may apply a threshold to make the most suitable areas 
        pop on your map.

3. Present your results in at least one figure for each grassland/climate 
scenario combination.


## Code

1. Use PEP 8 Style Standards
2. Functions have numpy-style docstrings
3. Make functions and/or loops DRY and modular
4. Well document the code with comments
