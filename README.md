
# OpenCV Image Manipulation Project

In this project, we are working with an image of a person and performing a series of manipulations using OpenCV to enhance, segment, and extract key features from the image.


# Operations to be Performed

## 1. Enhance the Contrast of the Image
    a) The goal is to improve the visibility of the image details by enhancing its contrast.

    b) We will use histogram equalization or other contrast enhancement techniques available in OpenCV to achieve this.


## 2. Extract the Mask of the Person
    a) We aim to extract the person from the image and create a mask that isolates the person from the background.

    b) This will involve applying thresholding techniques or segmentation methods to separate the foreground (person) from the background.


## 3. Extract the Edges of the Person
Two methods will be used to detect and extract edges around the person

    a) Morphological Operations: We will use morphological operations like dilation, erosion, and gradient to highlight the edges.

    b) Standard Edge Detector: We will apply a standard edge detection algorithm, such as the Canny Edge Detector, to extract clear edges of the person.

## 4. Segment the Image using GrabCut

We will apply OpenCV's GrabCut algorithm to segment the person from the background.

The GrabCut algorithm will help refine the segmentation, especially around finer details like hair and complex textures.

A rectangle will be drawn around the subject initially, and GrabCut will iteratively refine the segmentation using background and foreground modeling.


## Project Strucuture

``` bash
opencv_image_manipulation
│
├── notebooks/                        # Jupyter notebooks used for experimentation
│   └── image_manipulation_notebook.ipynb
├── reports/                          # Folder containing reports and results
│   └── figures/
│       └── potrait_lady.png           # Image file used for manipulation
├── scripts/                          # Python scripts for image manipulation
├── README.md                         # This file
└── requirements.txt                  # List of dependencies


```

## Instructions

Install dependencies

```bash
pip install -r requirements.txt
```

Run the image manipulation code at 
```
notebooks/image_manipualtion.ipynb
```







