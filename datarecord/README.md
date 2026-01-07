# Small Area UK Vegetation Indices (2025 EOX-based version)

These data provide Normalised Difference Vegetation Index (NDVI) and Enhanced Vegetation Index (EVI) statistics for each 2021 Lower Layer Super Output Area (LSOA) in England and Wales; 2021 Super Data Zone in Northern Ireland; and 2022 Data Zones in Scotland. These data have utility in themselves for a range of applications related to the measurement of exposure to green space, and are also a composite component of our Access to Healthy Assets and Hazards indicator. 

## Content 

Input to the NDVI and EVI statistics are derived from Sentinel-2 Cloudless imagery produced by EOX. By using cloud-free composites of Sentinel-2 data, vegetation metrics are calculated from averages of per-pixel NDVI and EVI values that are spatially joined to boundaries. The underlying EOX cloud free data relate to the year 2023 in this release with a 10m/pixel resolution. The vegetation indices are computed as follows: 

* NDVI = (NIR – Red) / (NIR + Red) 

* EVI = 2.5 * ((NIR – Red) / (NIR + 6 * Red – 7.5 * Blue + 1)) 

## Quality, Representation and Bias 

Full details of the data pipeline used to generate these statistics can be found on our GitHub page. It is worth noting that input pixel data noise is reduced by detecting and removing any pixel level NDVI values below -1 and above 1. When using NDVI in analysis, it is highly recommended to use the ‘NDVI_MEDIAN’ to mitigate for the effects of additional noise. Vegetation Fraction (‘VEG_FRAC’) is recommended for determining the cover of vegetation across LSOAs, whilst “greenness” can be determined through ‘NDVI’ or ‘EVI’ values. 

We develop these averaged measures primarily as an indicator of “greenness” for social science and public health related applications, and because the input data related to a cloudless mosaic, which can blend images from multiple different times of the year, these data may impact their use for any phenology-based studies.

Source code for this data is at https://github.com/GeographicDataService/ndvi/. The data itself, and supporting files, are listed above in this folder. 
