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

A) <img width="300" height="1083" alt="image" src="https://github.com/user-attachments/assets/52480720-3ea1-4898-b1f2-fdd756712959" />

B) <img width="300" height="1075" alt="image" src="https://github.com/user-attachments/assets/01638abf-94c1-4068-91c1-21d8044dd224" />

C) <img width="300" height="1070" alt="image" src="https://github.com/user-attachments/assets/54693b73-359a-4d67-a95f-a9e7d0dc6ba3" />

4) <img width="300" height="1031" alt="image" src="https://github.com/user-attachments/assets/ae0676d9-9fc9-491d-98db-2e036720f1ba" />


## Numpy-Kicking off with numpy

1) Import numpy as np

<img width="1785" height="1078" alt="image" src="https://github.com/user-attachments/assets/9dd1b811-7ead-402a-aafe-d4e171cd1806" />

























