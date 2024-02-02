# No Cameraman Left Behind

By Sindhura Mente, Sriya Reddi, Jeffrey Li, Amar Mohanty

Last Updated: December 15, 2022

## Project Summary

In this project, we address a universal issue in taking group pictures: leaving out the photographer. Having access to a source image of only the photographer and a target image of the rest of the group, we propose a program that can incorporate both parties into one realistic final output using open-source software, namely NumPy, OpenCV, and PyTorch. The image processing pipeline involves three major steps: (1) image segmentation of person(s), (2) information extraction from the source image, and (3) gradient domain blending. From qualitative tests, our program works well on images with people standing in front of a solid background and with people standing next to each other on the horizontal axis. The final product rivals the results manually produced using Adobe Photoshop software. The program performs suboptimally on images with complex backgrounds, with people standing at different locations in the foreground, and images taken at different angles. Future work can be done to improve the robustness of our program and to combat more edge cases.

<div style="display: flex; justify-content: space-between;">
    <img src="/Notebook/Images/Solid/source.jpg" width="200">
    <img src="/Notebook/Images/Solid/target.jpg" width="200">
    <img src="/Notebook/Images/Solid/groundtruth.jpeg" width="200">
    <img src="/Notebook/Results/solid.jpg" width="200">
</div>

From Left to Right: Source Image, Target Image, Photoshop Ground Truth, and Resulting Image.

<div style="display: flex; justify-content: space-between;">
    <img src="/Notebook/Images/Nonsolid/source.jpg" width="250">
    <img src="/Notebook/Images/Nonsolid/target.jpg" width="250">
    <img src="/Notebook/Results/nonsolid.jpg" width="250">
</div>

From Left to Right: Source Image, Target Image, and Resulting Image.

<div style="display: flex; justify-content: space-between;">
    <img src="/Notebook/Images/Sitting/source.jpg" width="250">
    <img src="/Notebook/Images/Sitting/target.jpg" width="250">
    <img src="/Notebook/Results/sitting.jpg" width="250">
</div>

From Left to Right: Source Image, Target Image, Photoshop Ground Truth, and Resulting Image.

<div style="display: flex; justify-content: space-between;">
    <img src="/Notebook/Images/Livedemo/source.jpg" width="250">
    <img src="/Notebook/Images/Livedemo/target.jpg" width="250">
    <img src="/Notebook/Results/livedemo.jpg" width="250">
</div>

From Left to Right: Source Image, Target Image, Photoshop Ground Truth, and Resulting Image.

## Content

- **Documents:** contains all of the typed deliverables
    - Final-report.pdf: six page final report
    - Slides: PowerPoint presentation from 12/07/2022 live demo
- **Logs:** contains all experimental, trials, and preprocessing steps we worked on prior to piecing together the final notebook (program)
    - Disclaimer: The notebooks in this section are mainly for showing the progress we made. They are not guaranteed to run.
    - image-placement: notebook for extracting points from source image, aligning person(s) in target image using Numpy and OpenCV modules
    - seamless: notebook for testing out and determining parameters for performing seamless cloning using previous assignment code and OpenCV modules
    - training-unet: notebook for training U-Net using PyTorch and Kaggle Supervise.ly person [image dataset](https://www.kaggle.com/datasets/tapakah68/supervisely-filtered-segmentation-person-dataset) 
- **Notebook:** contains the main program for our project
    - main.ipynb: notebook containing our source code **(RUN THIS)**
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
3.	**TODO:**
    - Setting Up Directory: Mount the notebook to your Google Drive
    - Define Source and Target Image: Choose your source and target images from the Images folder. Do not mix and match between folders.
    - Compare with Ground Truth: If you have a ground truth image (real image or Photoshopped Image), please add it here. If not, please ignore this section. There is only one Ground Truth image in our Images file, and it is Images/Solid/groundtruth.jpeg.
    - Save Output: Choose a name for your output file and save it to the Results folder.
