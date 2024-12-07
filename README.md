# Benthic Habitat Classification with Python

This workflow focuses on classifying benthic habitats, which is similar to land-use and land-cover (LULC) classification on terrestrial areas, but here the objects of interest are in shallow water environments. In certain scenarios, it is advisable to apply specific preprocessing steps to the satellite imagery, such as:

- **Atmospheric correction**  
- **Water column correction** (useful if the geomorphology is not relatively flat or reef flats)  
- **Sunglint correction** (to handle sunlight reflections on the water surface)  

For simplicity, this script assumes the satellite imagery is in optimal condition and does not require these corrections.

## Workflow Overview

The main steps for benthic habitat classification are organized into three separate `.ipynb` files:

1. **Prepare Training and Testing Sets**  
   - Extract pixel values and labels from sample data to create datasets for training and testing the model.

2. **Build a Machine Learning Model**  
   - Train a model to classify benthic habitat classes based on the training dataset.

3. **Apply the Model to Satellite Imagery**  
   - Use the trained model to predict benthic habitat classes across the entire satellite image.
