# 649-Group-8-Project
This repository contains all of the necessary files required to run our AI pipeline with a description of our code explained below

This code file implements a comparative deep learning pipeline to classify mosquito species using five distinct architectures: ResNet50, ConvNeXt Tiny, MobileNetV3, and Vision Transformers (ViT Base and Large). The workflow utilizes the timm library for transfer learning, applying white-balance correction and normalization to images before fine-tuning the models on a split of 85% training and 15% validation data. Following training, the code performs a comprehensive evaluation using confusion matrices, multi-class ROC curves, and classification reports to assess accuracy across 12 classes. Furthermore, it includes explainability modules that generate occlusion sensitivity maps to visualize model focus and t-SNE plots to analyze how different architectures cluster image features.

The dataset is aggregated from multiple sources stored in Google Drive, labeled as "VectorCam_images," covering specific species such as Anopheles (gambiae, funestus, stephensi, darlingi, nuneztovari, albimanus, coustani), Aedes (aegypti, albopictus), Culex, Mansonia, and non-mosquitoes. Specific data subsets identified include a general "all_labels.csv" collection, Colombian datasets for An. darlingi, nuneztovari, and albimanus, An. stephensi images from the University of Notre Dame, and An. coustani samples from Uganda. The script consolidates these varying CSVs and directory structures into a master dataframe, filtering out unused labels and organizing the files into a local directory structure for efficient loading.

To set-up, install, and run the code to get results that our report discussed, follow these steps:

1. Download the code file labeled '649_group8.ipynb' and the folder labeled 'VectorCam_images' (which should contain a subfolder name 'raw_images' that has 5 subfolders and a csv file within it).
2. Within Google Drive under My Drive, you will need to create a folder labeled '649_group8' and within that folder create a folder named 'FinalProject' and within that folder input the 'VectorCam_images' folder you downloaded earlier. This should create the following base file path that is necessary for the code to work (and can be changed within the code if you wish): '/content/gdrive/MyDrive/649_group8/FinalProject/VectorCam_images'.
3. Open the coding file using Google Colab
4. Select the desire run-time (a high powered GPU is recommended) and click run-all

The code should run as expected and take over an hour to run through the entire pipeline (from importing the images from your Google Drive to your local directory all the way to generating the tSNE plots).

Note: You will need to enable access to your Google Drive for this to run and, unless you have the Google Colab subscription that has background running, you will need to keep this running in your browser while your computer is on in order for the code to fully complete.
