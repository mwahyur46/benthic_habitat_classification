![Thumbnail Medium_English_2](https://github.com/user-attachments/assets/5b9f5481-5c07-4b96-86ee-af14e98f20bc)

# Benthic Habitat Classification with Python

This pipeline focuses on classifying benthic habitats, analogous to land-use and land-cover (LULC) classification in terrestrial environments. However, the objects of interest here are located in shallow water ecosystems. Depending on the dataset's quality and the study area's characteristics, specific preprocessing steps for satellite imagery may be required, such as:

- **Atmospheric correction**  
- **Water column correction** (recommended if the geomorphology varies significantly or includes reef slopes)  
- **Sunglint correction** (to mitigate sunlight reflections on the water surface)  

For simplicity, this repository assumes the satellite imagery is already in optimal condition, and no additional corrections are applied.

## Pipeline Overview

The classification process is organized into three main stages, each represented by a separate `.ipynb` file:

1. **Preparing Training and Testing Datasets**  
   - Extract pixel values and corresponding labels from sample points.  
   - Create balanced datasets for training and testing the model.

2. **Developing the Machine Learning Model**  
   - Train a classification model using the Extreme Gradient Boosting (XGBoost) algorithm.  
   - Perform hyperparameter tuning to optimize model performance.  

3. **Applying the Model to Satellite Imagery**  
   - Use the trained model to classify benthic habitat types across the entire satellite image.  
   - Generate output maps for visual interpretation and analysis.  
  
# Benthic Habitat Classes
The classification of benthic habitats refers to data from the [Allen Coral Atlas (ACA) - Benthic Habitat v2.0](https://developers.google.com/earth-engine/datasets/catalog/ACA_reef_habitat_v2_0#bands), which is also used as the label for the sample points dataset. Thus, the `id_sample` field in the file is aligned with the values from the ACA data, where:  

- 11: Sand  
- 12: Rubble  
- 13: Rock  
- 14: Seagrass  
- 15: Coral/Algae  
- 18: Microalgal Mats  

## Download Data

For the PlanetScope imagery dated July 8, 2024, you can download it from the following link. This is due to the file size limitations that GitHub can handle, save these files into the **Data** folder.
1. [Raw Data (harmonized with Sentinel-2)](https://1drv.ms/i/s!AhfNAWExLGYtr9gbfNRBhZ-ir4eP4g?e=efPRgm)
2. [Masked shallow water only](https://1drv.ms/i/s!AhfNAWExLGYtr9hR8xpdtQSUH_seGA?e=NWheNZ)

#### Connect with me:
[LinkedIn](https://www.linkedin.com/in/mwahyur) [Medium](https://wahyu-ramadhan.medium.com)
