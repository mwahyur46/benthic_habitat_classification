![Thumbnail Medium_English_2](https://github.com/user-attachments/assets/5b9f5481-5c07-4b96-86ee-af14e98f20bc)

# Benthic Habitat Classification with Python

This workflow focuses on classifying benthic habitats, which is similar to land-use and land-cover (LULC) classification on terrestrial areas, but here the objects of interest are in shallow water environments. In certain scenarios, it is advisable to apply specific preprocessing steps to the satellite imagery, such as:

- **Atmospheric correction**  
- **Water column correction** (useful if the geomorphology is not relatively flat or reef flats)  
- **Sunglint correction** (to handle sunlight reflections on the water surface)  

For simplicity, this script assumes the satellite imagery is in optimal condition and does not require these corrections.

## Workflow Overview

The main steps for benthic habitat classification are organized into three separate `.ipynb` files:

1. **Prepare Training and Testing Dataset**  
   - Extract pixel values and labels from sample data to create datasets for training and testing the model.

2. **Build a Machine Learning Model**  
   - Build a model to classify benthic habitat classes based on the training dataset using the Extreme Gradient Boosting (XGBoost) algorithm.

3. **Apply the Model to Satellite Imagery**  
   - Use the trained model to predict benthic habitat classes across the entire satellite image.
  
# Benthic Habitat Classes
The classification of benthic habitats refers to data from the [Allen Coral Atlas (ACA) - Benthic Habitat v2.0](https://developers.google.com/earth-engine/datasets/catalog/ACA_reef_habitat_v2_0#bands), which is also used as the label for the sample points dataset. Thus, the `id_sample` field in the file is aligned with the values from the ACA data, where:  

- 0: Unmapped  (not included)
- 11: Sand  
- 12: Rubble  
- 13: Rock  
- 14: Seagrass  
- 15: Coral/Algae  
- 18: Microalgal Mats  

## Download Data

For the PlanetScope imagery dated July 8, 2024, you can download it from the following link. This is due to the file size limitations that GitHub can handle, save these files into the **Data** folder.
1. [Raw Data (harmonized with Sentinel-2](https://1drv.ms/i/s!AhfNAWExLGYtr9gbfNRBhZ-ir4eP4g?e=efPRgm)
2. [Masked shallow water only](https://1drv.ms/i/s!AhfNAWExLGYtr9hR8xpdtQSUH_seGA?e=NWheNZ)

#### Connect with me:
[LinkedIn](https://www.linkedin.com/in/mwahyur) [Medium](https://wahyu-ramadhan.medium.com)
