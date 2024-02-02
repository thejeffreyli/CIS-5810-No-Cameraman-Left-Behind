# No Cameraman Left Behind

By Sindhura Mente, Sriya Reddi, Jeffrey Li, Amar Mohanty

Last Updated: December 15, 2022

## Content

- Documents: contains all of the typed deliverables
    - Final-report.pdf: six page final report
    - Slides: PowerPoint presentation from 12/07/2022 live demo
- Logs: contains all experimental, trials, and preprocessing steps we worked on prior to piecing together the final notebook (program)
    - Disclaimer: The notebooks in this section are mainly for showing the progress we made. They are not guaranteed to run.
    - image-placement: notebook for extracting points from source image, aligning person(s) in target image using Numpy and OpenCV modules
    - seamless: notebook for testing out and determining parameters for performing seamless cloning using previous assignment code and OpenCV modules
    - training-unet: notebook for training U-Net using PyTorch and Kaggle Supervise.ly person [image dataset](https://www.kaggle.com/datasets/tapakah68/supervisely-filtered-segmentation-person-dataset) 
- Notebook: contains the main program for our project
    - main.ipynb: notebook containing our source code (PLEASE RUN THIS)
    - model.pt: working, trained U-Net model based in PyTorch
    - Images: contains different types of images used as source or target 
    - Results: contains working results from our program

## Program and System Requirements

We developed this primarily on Google Colab, using Python, PyTorch, and CUDA GPU.

Packages to Install:

```
pip install numpy
pip install Pillow
pip install torch
pip install torchvision
pip install segmentation-models-pytorch
pip install albumentations
pip install tqdm
pip install matplotlib
pip install opencv-python
pip install scikit-image

```

## How to Run

After you satisfy all the requirements mentioned above, there are some steps you need to do before running the notebook. 
1.	Ensure that the main.ipynb is mounted at your Google Drive.
2.	There are several sections labeled [TODO]. There will be instructions on each [TODO] section. Be sure that the directories are appropriately named according to read images from the Images folder. The same applies to saving the images into the Results folder.
3.	TODO:
    - Setting Up Directory: Mount the notebook to your Google Drive
    - Define Source and Target Image: Choose your source and target images from the Images folder. Do not mix and match between folders.
    - Compare with Ground Truth: If you have a ground truth image (real image or Photoshopped Image), please add it here. If not, please ignore this section. There is only one Ground Truth image in our Images file, and it is Images/Solid/groundtruth.jpeg.
    - Save Output: Choose a name for your output file and save it to the Results folder.
