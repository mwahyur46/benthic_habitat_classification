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
   - Train a model to classify benthic habitat classes based on the training dataset.

3. **Apply the Model to Satellite Imagery**  
   - Use the trained model to predict benthic habitat classes across the entire satellite image.

### Download Data

For the PlanetScope imagery dated July 8, 2024, you can download it from the following link. This is due to the file size limitations that GitHub can handle, save these files into the **Data** folder.
1. RAW data (harmonized with Sentinel-2): https://1drv.ms/i/s!AhfNAWExLGYtr9gbfNRBhZ-ir4eP4g?e=efPRgm
2. Masked shallow water only: https://1drv.ms/i/s!AhfNAWExLGYtr9hR8xpdtQSUH_seGA?e=NWheNZ

![Story Preview_export fix](https://github.com/user-attachments/assets/a4ea867c-eb3f-4df6-b242-48178766c047)
