# Image Geometric Transformations (Rotation & Skewing)

This Jupyter notebook (`1 Transformation.ipynb`) demonstrates how to implement basic geometric image transformations from scratch using bilinear interpolation, without relying on OpenCV’s built-in warp functions.

---

## Contents

1. **Problem Statement**  
   A brief description of the task: write functions to rotate and skew (shear) an input image by arbitrary angles, using bilinear interpolation for resampling.

2. **Environment Setup**  
   - Installs the required package:
     ```bash
     pip install opencv-python
     ```
   - Imports:
     ```python
     import cv2
     import numpy as np
     import matplotlib.pyplot as plt
     ```

3. **Bilinear Interpolation**  
   ```python
   def bilinear_interpolation(image, new_x, new_y):
       # Given floating‐point coordinates (new_x, new_y),
       # compute the interpolated pixel value from the 4 surrounding pixels.
