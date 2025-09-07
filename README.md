# Autovit-OpenCV
OpenCV Workshop (Sep 2025)


## Numpy-Why is numpy used in open Cv?

<img width="300" height="1196" alt="image" src="https://github.com/user-attachments/assets/6017f877-0fed-4929-872c-c696bcddaaab" />

1. Images = Arrays
   
   In OpenCV, images are represented as NumPy arrays — specifically, numpy.ndarray.

   Each pixel is a numerical value (grayscale: 1 channel, color: 3 channels), so treating images as arrays makes processing intuitive and efficient.

```c
import cv2

import numpy as np


img = cv2.imread('photo.jpg')

print(type(img))  # <class 'numpy.ndarray'>

```

2. Fast Mathematical Operations

   NumPy is optimized for vectorized operations, which means it can process entire arrays without explicit loops.

   Used to perform tasks like:

    • Brightness/contrast adjustments

    • Filtering and convolution

    • Thresholding and masking

```c
brighter = img + 50  # Adds 50 to every pixel value

```

3. Seamless Integration
   
   OpenCV functions return NumPy arrays, so you can directly use NumPy methods like .reshape(), .mean(), .sum(), etc.

   You can also slice and index images just like any array:
   
```c
roi = img[100:200, 150:250]  # Region of interest
```

4. Custom Filters and Manipulations
   
   Want to build your own kernel for edge detection or blur? NumPy makes it easy to define and apply custom matrices.

```c
kernel = np.array([[0, -1, 0],
                   [-1, 5,-1],
                   [0, -1, 0]])
sharpened = cv2.filter2D(img, -1, kernel)
```


















