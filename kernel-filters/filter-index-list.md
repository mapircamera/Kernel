#Multi-Spectral Camera Indices

Below are various indices commonly used for processing lower altitude (UAS/drone) multi-spectral imagery that often does not need to correct for higher altitude (satellite) atmospheric influences such as aerosol.
***************************************************************
##Broadband Vegetation Indices

###Normalized Difference Vegetation Index (NDVI)
This index is a measure of healthy, green vegetation. The combination of its normalized difference formulation and use of the highest absorption and reflectance regions of chlorophyll make it robust over a wide range of conditions. It can, however, saturate in dense vegetation conditions when leaf area index (LAI) becomes high. See the following indices for better results.  
![](/assets/SpectralIndexFormulaNDVI.gif)  

Suggested Kernel Filters:  
NIR = [F850](https://www.mapir.camera/collections/kernel-camera-filters/products/f850)  
RED = [F650](https://www.mapir.camera/collections/kernel-camera-filters/products/f650)

###Enhanced Vegetation Index (EVI)
This index was developed as a standard MODIS product to improve the NDVI by optimizing the vegetation signal in LAI regions. It uses the blue reflectance region to correct for soil background signals and to reduce atmospheric influences, including aerosol scattering. It is most useful in LAI regions where the NDVI may saturate.  
![](/assets/SpectralIndexFormulaEVI.gif)  

Suggested Kernel Filters:  
NIR = [F850](https://www.mapir.camera/collections/kernel-camera-filters/products/f850)  
RED = [F650](https://www.mapir.camera/collections/kernel-camera-filters/products/f650)  
BLUE = [F450](https://www.mapir.camera/collections/kernel-camera-filters/products/f450)

###Modified Simple Ratio (MSR)
This index was developed an an improvement over RDVI by combining the Simple Ratio into the formula. The RDVI index uses the difference between near-infrared and red wavelengths, along with the NDVI, to highlight healthy vegetation. It is insensitive to the effects of soil and sun viewing geometry. The MSR index has increased sensitivity to vegetation biophysical parameters.  
![](/assets/SpectralIndexFormulaMSR.gif)  

Suggested Kernel Filters:  
NIR = [F850](https://www.mapir.camera/collections/kernel-camera-filters/products/f850)  
RED = [F650](https://www.mapir.camera/collections/kernel-camera-filters/products/f650)

###Optimized Soil Adjusted Vegetation Index (OSAVI)
This index is based on the Soil Adjusted Vegetation Index (SAVI), which is similar to NDVI, but suppresses the effects of soil pixels. OSAVI uses a standard value of 0.16 for the canopy background adjustment factor (L). Rondeaux (1996) determined that this value provides greater soil variation than SAVI for low vegetation cover, while demonstrating increased sensitivity to vegetation cover greater than 50%. This index is best used in areas with relatively sparse vegetation where soil is visible through the canopy.  
![](/assets/SpectralIndexFormulaOSAVI.gif)  

Suggested Kernel Filters:  
NIR = [F850](https://www.mapir.camera/collections/kernel-camera-filters/products/f850)  
RED = [F650](https://www.mapir.camera/collections/kernel-camera-filters/products/f650)

###Transformed Difference Vegetation Index (TDVI)
This index is useful for monitoring vegetation cover in urban environments. It does not saturate like NDVI and SAVI.  
![](/assets/SpectralIndexFormulaTDVI.gif)  
Suggested Kernel Filters:  
NIR = [F850](https://www.mapir.camera/collections/kernel-camera-filters/products/f850)  
RED = [F650](https://www.mapir.camera/collections/kernel-camera-filters/products/f650)

###Leaf Area Index (LAI)
This index is used to estimate foliage cover and to forecast crop growth and yield. Where EVI is the Enhanced Vegetation Index value.  
![](/assets/SpectralIndexFormulaLAI.gif)  
![](/assets/SpectralIndexFormulaEVI.gif)  

Suggested Kernel Filters:  
NIR = [F850](https://www.mapir.camera/collections/kernel-camera-filters/products/f850)  
RED = [F650](https://www.mapir.camera/collections/kernel-camera-filters/products/f650)  
BLUE = [F450](https://www.mapir.camera/collections/kernel-camera-filters/products/f450)

###Green Normalized Difference Vegetation Index (GNDVI)
This index is similar to NDVI except that it measures the green spectrum from 540 to 570 nm instead of the red spectrum. It is sometimes called the "greeness" index. This index is more sensitive to chlorophyll concentration than NDVI.  
![](/assets/SpectralIndexFormulaGNDVI.gif)  

Suggested Kernel Filters:  
NIR = [F850](https://www.mapir.camera/collections/kernel-camera-filters/products/f850)  
RED = [F550](https://www.mapir.camera/collections/kernel-camera-filters/products/f550)
***************************************************************
##Mineral Indices

###Iron Oxide Ratio
This band ratio highlights hydrothermally altered rocks that have been subjected to oxidation of iron-bearing sulphides.  
![](/assets/SpectralIndexFormulaIronOxide.gif)  

Suggested Kernel Filters:  
RED = [F650](https://www.mapir.camera/collections/kernel-camera-filters/products/f650)  
BLUE = [F490](https://www.mapir.camera/collections/kernel-camera-filters/products/f490)

###WorldView New Iron Index (WV-II)
This index uses WorldView-2 bands to identify pixels rich in iron oxide.  
![](/assets/SpectralIndexFormulaWV-II.gif)  

Suggested Kernel Filters:  
GREEN = [F550](https://www.mapir.camera/collections/kernel-camera-filters/products/f550)  
YELLOW = [F615](https://www.mapir.camera/collections/kernel-camera-filters/products/f615)  
BLUE = [F490](https://www.mapir.camera/collections/kernel-camera-filters/products/f490)

###WorldView Soil Index (WV-SI)
This index uses WorldView-2 bands to identify pixels that primarily consist of soil.  
![](/assets/SpectralIndexFormulaWV-SI.gif)  

Suggested Kernel Filters:  
GREEN = [F550](https://www.mapir.camera/collections/kernel-camera-filters/products/f550)  
YELLOW = [F615](https://www.mapir.camera/collections/kernel-camera-filters/products/f615)

***************************************************************
##Fire/Burn Region Indices

###Burn Area Index (BAI)
This index highlights burned land in the red to near-infrared spectrum, by emphasizing the charcoal signal in post-fire images. The index is computed from the spectral distance from each pixel to a reference spectral point, where recently burned areas converge. Brighter pixels indicate burned areas.  
![](/assets/SpectralIndexFormulaBAI.gif)  
Suggested Kernel Filters:  
NIR = [F850](https://www.mapir.camera/collections/kernel-camera-filters/products/f850)  
RED = [F550](https://www.mapir.camera/collections/kernel-camera-filters/products/f550)


***************************************************************
#####References:
_Please browse the sites below which refer to their own further references:_

Harris Geospatial Solutions: https://www.harrisgeospatial.com