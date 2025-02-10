Please note that this repository does not contain the TIFF file. You will need to run Sentinel GeoTIFF ipynb first to download the processed tiff. (The original S2 Tiff provided by the challenge only contains 4 bands, but I included all the available bands. So the Sentinel 2 ipynb is a bit different than the one provided by the challenge.) 

data_s2 and sub_s2 refers to the train and submission data that combines weather / building footprints / sentinel 2 information. This is done through UHI Preprocessing ipynb.This notebook only maps and combines the data and did not do any other feature engineer tasks. 

Please also note that the NDVI is only calculated in the Final Experiment ipynb. Some other feature engineering may also only happened in the Final Experiment ipynb. 

Before running any of these notebooks, please download the orginal datasets yourself. If there is an error while running, it is most likely directory issue, please change according to your own file locations.

# Things to do:
1. Tune the buffer size for buildings footprints, may try to set different buffer size for different region
2. Try different models
3. Combine Landsat tiff data
4. If Landsat tiff is available, think of how to use both sentinel 2 and landsat. Do we combine both data and recalculate it (e.h. average of 2?)
5. Any other possible features
   

