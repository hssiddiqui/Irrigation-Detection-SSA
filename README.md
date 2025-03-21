# Smallholder Irrigation Detection

## Repository Structure

The repository contains scripts and files for small holder irrigation detection across sub-Saharan Africa

```
Irrigation-Detection/
├── data-collection-polygons/                     # Folder for input files
│   └── ......                   
├── GEE_scripts/                                  
│   └── Interactive_EVI_Extraction.js             # View Sentinel 2 EVI time series for polygons    
├── Google_colab_scripts/
    ├── s2_imagery_upload.ipynb                   # Download S2 EVI stack
    ├── clean_labelled_data.ipynb                 # Cluster cleaning script
    ├── smooth_inference_imagery.ipynb            # Svatisky Golay Filter for smoothing 
    ├── irrigation_detection_inference.ipynb      # Run irrigation predictions on EVI stack
    └── utils.ipynb                               # Utility functions
└── Sahel_labeling_v4.pdf
```
