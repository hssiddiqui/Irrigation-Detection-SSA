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
> [!NOTE]
> Users can skip steps 1-4 and use the trained models to detect dry season irrigation in Nigeria or Burkina Faso

1. **Collect labeled data for training:**
     ```
     GEE_scripts/Interactive_EVI_Extraction.js
     ```
   - [Open script in Google Earth Engine](https://code.earthengine.google.com/d3ed4fa2bcebafc63eca0e6db15d1db0)
   - Draw polygons by looking at high resolution Google Earth imagery and false color composites of dry season S2 imagery 
   - Examine S2 EVI time series
   - Save 

2. **Create Sentinel 2 EVI stack:**
    ```
    Google_colab_scripts/s2_imagery_upload.ipynb
    ```

3. **Clean labelled data:**
   ```
   Google_colab_scripts/clean_labelled_data.ipynb
   ```

4. **Train models:**
    - [Detecting Irrigation in the Ethiopian Highlands](https://github.com/SEL-Columbia/ethiopia_irrigation_detection)

5. **Download and smooth inference imagery:**
    ```
     Google_colab_scripts/s2_imagery_upload.ipynb
     Google_colab_scripts/smooth_inference_imagery.ipynb
     ```

6. **Irrigation Detection:**
    ```
     Google_colab_scripts/irrigation_detection_inference.ipynb
     ```