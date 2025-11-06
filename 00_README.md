# sgg00425-stac

This is the code repository for the course SGG.00425 "Environmental data and methods". 

You can either download it as a zip file (green "Code" button), or clone it with "git":
git clone https://github.com/pohleric/sgg00425-stac.git

## Evironment

`conda activate pystac_example`

`conda deactivate`

## Install
Follow the instructions given in the file 
**Anaconda-Installation (personal computer)[optional]**. You find this file on **Moodle**.
> The folder name might be different, e.g. "sgg.00425", "SGG.00425" , etc. This is not a problem. Adjust the folder name if you get an error that the folder name is not correct.


## Data

This code repository is lacking all data. Please download the entire data folder called "data" and place this folder into the main folder "sgg00425-stac". Download the data here:

https://unifrch-my.sharepoint.com/:f:/g/personal/eric_pohl_unifr_ch/Ek-aWar-91tBsNOdhSnu--ABiN52AgShUQJuz4Nn0-OOXA?e=Cdtxp0


## Notes from the session 

for help: see ~/help
also: setting > Contextual help 

Jupyter shortcuts: [a] +above, [b] +below, [d][d] delete

# Env and geospatial data: 

raster and vectors -> coordinates and projections (3D->2D) what infromation gets preserved? 

** make sure units of measurements line up 

1. vectors: coordinates (x, y) ^ lines ^ polygons (start & end)
2. raster data: grids of satellite images, in matrices, in varied resolutions 

## In a GIS: layers 

Usual: layers of vector and raster, derived in different ways, the link between them are spatial dimensions 

Spatio-TEMPORAL data: 
- Observation data: 
    - satellite images (like the demand cube)
- Reference Dimensions 
    - raster lat
    - raster long 
    - vector time?


Data represented? 
1. land parcels : `vector`
2. Land Cover and Land Use : `raster`
3. Geology and Soils : ?? cube? 


Land Use:  3x version /year (land use classes)
1. agri > meadows, farm pasterus > meadows
2. unproductive > unproductive vegetation

Visually examine & quantify changes (DATA TYPES)

# Multi-Spectral Remote Sensing 

## Electromagnetic Radiation 

Radiation: measure and analysis of electromagnetic radiation — moves at light speed through a vacuum 
- variance between 300km/s to 100km/s due to the type of material (e.g. ice) light is moving through 
- thermal radiation of charged particles in matter, every body with temperature not absolute 0 (kelvin) emits radiation
- radiation intensity (energy emits) X wavelength (cooler = longer wavelength) 
- body: Emitted radiation (temperature and emissivity), reflected radiation (passively reflected, function of surface of body independent of temperature)

Radiation and atmosphere
- electromagnetic radiation: absorbed or scatted on path 
- transparent: atmospheric windows (how much of the radiation can penetrate atmosphere depends on the wavelengths & which gasses absorb the wavelengths)
- visible spectrum: peak of solar radiation
- absorption or scattering for another time 

## sensors, platforms, and orbits 

sky.rogue.space > geostationary orbit, make revolution in 1 day : we look at `landsat 8` and maybe `sentinel 2a` -- 100 min for revolution
<!-- voyager -->

Landsat 1972 - present 
remote sensing allows 'unrestricted access' 

- geostationary orbit has to be around equator
- satellite passes over each point of earth at the same time 
- inclination: orbital trach vs equation angle 

Image sensors: 
- optical lenses used to creatteimage of object on projection surface 
- electromacgnetic radiation refracted by lens and focused on projection of surface
- light cells: pixels. measure intensity of radiation with several layers, make an analog signal which gets turned into digital signal 

1. object rhough lens 
2. birghtness measure on pixes 
3. analog to digital converstion on pixel
4. conversion to image

phone is multispectral: different sensors/channel measure 1 colour, combined --- more advanced compares along the wavelengths 
- visual and short wave infrared 
- Landsat works with bands, can use tables to see which part of electromagnetic spectrum represented by different bands  (like inkscape!)
- convention: B&W for 3 primary colours where white is high intensity, and dark is low intensity

### visualising the invisible -- mosaicing spectral bands 

using variables from outside the visible spectrum, but can only visualise results from within the visible spectrum 

1. earth point 
2. sensor picks up the electromagnetic radiation 
3. represented as radiation intensity per band measured on pixel level  (sub-pixel in RGB)
4. for each pixel: RGB, NearIR and SWIR 

### Magic of Glacier Mapping 

rock surfaces vs snow: rock similar reflectivity across entire range, whereas glacier ice bright in visual, dull in infra-red. 
Reflectivity across bands useful for mapping what we are looking at. 
e.g. D = red / SWIR

mask through threshold and can convert to outlines (literally the same as the tracing on inkscape)

# Stickies: 

### 06/11 10:52

good: nice overview, keyboard shortcuts are fun
bad: Jupyter lab is ugly

### 06/11 11:49 

one of the most interesting lectures I've attended, really nice.
