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
6. Experiment with different features combination to train.
7. Need to try not shuffling the train data for model training (because the dataset might be time series dependednt, shuffling might make it worse)

### Findings (feel free to still use it even when mine seems to be not useful):
1. Weather data: Only solar flux and wind direction is found to make improve the model
2. Footprints: Only nearest building distance and building density is useful
3. S2 Tiff: NDVI seems to make it worse.
4. So far, these are the best features for the current RF model:  "building_density", "SB01", "SB03", "nearest_building_distance", "Wind Direction", "Solar Flux"
5. RF model is the best (XGBoost and LightBGM is worse)
6. I coded a ANN model but it performs super badly, can explore other deep learning models but I doubt it might be good.

   

