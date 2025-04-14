# Smallholder Irrigation Detection

## Repository Structure

The repository contains scripts and files for small holder irrigation detection across sub-Saharan Africa

```
Irrigation-Detection/
├── data-collection-polygons/                     # Folder for input files
│   └── ...... 
├── trained-models/                               # Trained transformer models
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

## How to implement the methodology

1. **Collect labeled data for training:**
   Use GEE_scripts/Interactive_EVI_Extraction to draw polygons, examine high resolution Google Earth imagery, false color composite of dry season imagery and S2 time series

2. **Create Sentinel 2 EVI stack:**
   - s2_imagery_upload.ipynb

3. **Clean labelled Data:**
   - clean_labelled_data.ipynb

4. **Irrigation Detection:**
   - Execute the main script:
     ```bash
     Google_colab_scripts/irrigation_detection_inference.ipynb
     ```