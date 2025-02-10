Please note that this repository does not contain the TIFF file. You will need to run Sentinel GeoTIFF ipynb first to download the processed tiff. (The original S2 Tiff provided by the challenge only contains 4 bands, but I included all the available bands. So the Sentinel 2 ipynb is a bit different than the one provided by the challenge.) 

data_s2 and sub_s2 refers to the train and submission data that combines weather / building footprints / sentinel 2 information. This is done through UHI Preprocessing ipynb.This notebook only maps and combines the data and did not do any other feature engineer tasks.

Please also note that the NDVI is only calculated in the Final Experiment ipynb. Some other feature engineering may also only happened in the Final Experiment ipynb. 



