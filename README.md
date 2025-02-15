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

1. **Data Preprocessing**:
    - Regrid TROPOMI SIF with different quality filtering criteria, test sensitivity of 8-day time series at Kapiti
      - `tropomi_sensitivity.R`
      - `SIFtotal.R`
    - Regrid all satellite datasets to 0.15 degree
        - `intra_annual_region.R`
        - `intra_annual_region_regridding.R`
    - Extract satellite data at the site location
        - `extract_data.R`
    - Calculate multiyear average of LST, NIRv, Precip, SM in HoA
        - `multiyear_region.R`
    - Extract multiyear average at Kapiti
        - `multiyear_site.R`
    - Evaluate spatial heterogeneiity around the site location
        - `heterogeneity.R`
2. **Evaluation of satellite SIF datasets with in-situ SIF**:
    - This part was conducted by Dr. Giulia Tagliabue and the scripts are not included in this repository.
3. **Intra-seasonal dynamics at Kapiti**:
    - Evaluate vegetation dynamics at Kapiti between October 2019 and February 2020. 
        - `intra_annual_site.R`
        - `intra_annual_site_NIRvP.R`
4. **Intra-seasonal dynamics for the entire HoA drylands**
        - `intra_annual_region_combinedplot_longperiod.R`
        - `intra_annual_region_combinedplot.R`
        - `intra_annual_region_combinedplot_met.R`
        - `intra_annual_region_subregions.R` 
        - `intra_annual_region_subregions_subperiods.R`
        - `intra_annual_region_subregions_subperiods_sifyield.R`
5. **Figures in the manuscript**:
    - Figure 1: 1b - `MODIS_LC.R`; 1c, 1d, 1e - `multiyear_region.R`; 1h - `multiyear_site.R`
    - Figure 2: N/A
    - Figure 3: `intra_annual_site.R`
    - Figure 4: ``
    - Figure 5-6: `intra_annual_region_combinedplot.R`
    - Figure 7: `intra_annual_region_subregions_subperiods.R`

    - Figure S1: `heterogeneity.R`
    - Figure S2: N/A
    - Figure S3: `tropomi_sensitivity.R`
    - Figure S4: `intra_annual_site_NIRvP.R`
    - Figure S5: N/A
    - Figure S6-S7: `intra_annual_region_combinedplot_longperiod.R`
    - Figure S8-S11: `intra_annual_region_combinedplot.R`
    - Figure S12: `intra_annual_region_subregions_subperiods_sifyield.R`

## Contact

For any questions or issues, please contact jwen@carnegiescience.edu.
