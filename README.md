# Class agnostic feature learning- (using class agnostic activation map)

## ISIC 2019 image dataset preparation
This repository outlines the process for preparing the ISIC 2019 dataset for training and evaluation purposes.

Step 1: Combine Train and Validation Sets
First, download the Train and Validation datasets from the ISIC 2019 challenge. Combine these two datasets to create the entire dataset for the study.

Step 2: Focus on Relevant Labels
In this study, we focused on detecting melanoma, which is a critical dermatological condition. Therefore, we only used the images labeled as melanoma (MEL) and nevus (NV) from the ISIC 2019 dataset.

Step 3: Split the Dataset
After filtering the dataset to include only the relevant labels, the data is split into three subsets:

Test set: 2000 images
Validation set: 1000 images
Train set: Remaining images
This split ensures a sufficient number of samples for training, validation, and testing.

Step 4: Save Metadata in JSON or Pickle Format
The dataset's image filenames and labels are saved in a structured format, such as a JSON or pickle file, for easy loading during training and evaluation. Below is an example of a JSON file structure:

[
   
    {"image": "ISIC_0028049", "label": "NV"},
    
    {"image": "ISIC_0060326", "label": "MEL"},
    
    {"image": "ISIC_0014851_downsampled", "label": "NV"},
    ...
]

## Installation

To install the required dependencies for this project, use the following command:

```bash
pip install -r requirements.txt
```
##  Traning Loss

CE1 Loss: Cross-Entropy Loss for the original image

CE2 Loss: Cross-Entropy Loss for the transformed image

CAAM Loss: Loss between the transformed original CAAM and the CAAM of the transformed image

