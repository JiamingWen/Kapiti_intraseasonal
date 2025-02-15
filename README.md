# Kapiti_intraseasonal

## Overview

This repository contains code for analyzing fast-changing intra-seasonal vegetation dynamics of drylands in the Horn of Africa (HoA) using solar-induced chlorophyll fluorescence (SIF) (Wen et al., 2025 Biogeosciences). In this study, We found that SIF from TROPOspheric Monitoring Instrument (TROPOMI) with daily revisit frequency identified highly dynamic week-to-week variations in both shrublands and grasslands; such rapid-changing vegetation dynamics corresponded to the up- and down- regulation by the fluctuations of environmental variables (e.g., air temperature, vapor pressure deficit, soil moisture). However, neither reconstructed SIF products nor near-infrared 
reflectance of terrestrial vegetation (NIRv) from Moderate Resolution Imaging Spectroradiometer (MODIS), which is widely used in literature, was able to capture such fast-changing intra-seasonal variations.

Details about this study can be found at: https://egusphere.copernicus.org/preprints/2024/egusphere-2024-2529/egusphere-2024-2529.pdf

## Data
- In situ SIF
- Satellite vegetation datasets
    - TROPOMI SIF
    - Reconstructed SIF products: CSIF, GOSIF, SIF_oco2_005
    - MODIS NIRv
- Climate variables:
    - CHIRPS precipitation, ESA-CCI soil moisture, MERRA-2 Air temperature (Tair), water vapor pressure deficit (VPD) and photosynthetically active radiation (PAR)
 
## Analysis Steps

1.
2. **Data Preprocessing**:
    - Regrid TROPOMI SIF with different quality filtering criteria, test sensitivity of 8-day time series at Kapiti
      - `tropomi_sensitivity.R` 
    - Regrid satellite data
        - ``
    - Extract satellite data at the site location
        - ``
        - ``
2. **Evaluation of satellite SIF datasets with in-situ SIF**:
    - This part was conducted by Dr. Giulia Tagliabue and the scripts are not included in this repository.
4. **Intra-seasonal dynamics at Kapiti**:
5. **Intra-seasonal dynamics for the entire HoA drylands**
6. **Other analyses**
    - Test sensitivity of applying different quality filtering criteria for TROPOMI SIF
  
6. **Figures in the manuscript**:
    - Figure 1: ``
    - Figure 2: ``
    - Figure 3: ``
    - Figure 4: ``
    - Figure 5: ``
    - Figure 6: ``
    - Figure 7: ``
    - 
    - Figure S1: ``
    - Figure S2: ``
    - Figure S3: `tropomi_sensitivity.R`
    - Figure S4: ``
    - Figure S5: ``
    - Figure S6: `` 
    - Figure S7: ``
    - Figure S8: ``
    - Figure S9: ``
    - Figure S10: ``
    - Figure S11: ``
    - Figure S12: ``
