# Deepfake-Detection

CS 4644 / 7643 Deep Learning - Final Project

This repository includes a variety of deep learning approaches for identifying artificially generated media content, including images, videos, and audio recordings seeking to mitigate the consequences of the proliferation of deepfake content in online spaces.

05/01/2024

## Description

This repository includes all of our code for the final project in CS 7643 - Deep Learning, where we focused on examining models for Deepfake Detection. We looked at two existing models for image deepfake detection, the CNN-based Xception and a Visual Transformer model, and created a novel 3D CNN model to detect deepfake videos.

### Files

- images - folder containing generated analysis charts for the models
- ViT - folder containing notebooks and files relating to the Visual Transformer Model
  - models - folder containing the saved ViT models
    - 10k - saved ViT model trained on smaller, 10k image dataset
    - 140k - saved ViT model trained on larger, 140k image dataset
  - 10k_ViT.ipynb - notebook for training, saving, and loading smaller ViT model
  - 140k_ViT.ipynb - notebook for training, saving, and loading larger ViT model
  - requirements.txt - requirements file to train and run ViT models
- Xception - folder containing notebooks and files relating to the Xception Model
  - Xception 10k Model - saved Xception model trained on smaller, 10k image dataset
    - predictions.npy - array of prediction classes for 10k test
    - true_labels.npy - array of ground truths for 10k test
  - xception10k.ipynb - notebook for training, saving, and loading smaller ViT model
  - xception140k.ipynb - notebook for training, saving, and loading larger ViT model
  - requirements.txt - requirements file to train and run Xception models
- data_extraction.ipynb - notebook for initial data restructuring and manipulation
- novel_video_audio.ipynb - notebook for the video and audio deepfake detection model

### Datasets

Retrieve 10k dataset zip from this link: https://www.kaggle.com/datasets/sachchitkunichetty/rvf10k/

Retrieve 140k dataset zip from this link: https://www.kaggle.com/datasets/xhlulu/140k-real-and-fake-faces/

Retrieve video dataset zip from this link: https://www.kaggle.com/competitions/deepfake-detection-challenge/data

Store the retrieved zips in the project folder, and run data_extraction.ipynb to prepare the two image datasets. The video dataset doesn't need any preparation and can be manually extracted. We also downloaded only the train videos rather than the entire dataset due to size limitations.

## Usage

Navigate to the project directory in the conda command prompt, and cd into ViT or Xception if you want to run either of those models. For those two models, there are included requirements.txt files to setup a conda environment. To do so, first create a new envioronment:

```bash
>> conda create -n <env_name> python=3.10

>> conda activate <env_name>
```

From here, make sure pip is installed using the following line, and afterwards install the requirements needed:

```bash
>> conda install pip

>> pip install -r requirements.txt
```

After that, you should be able to run the notebooks!

> > > > > > > Stashed changes
