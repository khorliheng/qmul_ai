# Texture Classification with Local Binary Patterns

This notebook (`4 Texture Classification.ipynb`) demonstrates how to extract texture features from grayscale images using Local Binary Patterns (LBP), build class‐specific descriptors via LBP histograms over sliding windows, and classify new images (faces vs. cars) by comparing histogram intersections.

---

## Contents

1. **Setup & Imports**  
2. **Utility Functions**  
   - `histogram_equalization(img)` – for visualizing window contrast  
   - `compute_LBP(img, window_size)` – sliding‐window LBP extraction with per‐window histograms & plots  
   - `histogram_intersection(hist1, hist2)` – similarity measure  
   - `classification(new_images, face_desc, car_desc)` – assigns “face” or “car” based on max histogram intersection  
3. **Building Class Descriptors**  
   - Load one face (`face-3.jpg`) and one car (`car-3.jpg`) image  
   - For a chosen `window_size`, extract LBP histograms and select a few representative windows as your class “dictionary”  
4. **Testing & Classification**  
   - Define a set of **new** images (`face-1.jpg`, `face-3.jpg`, `car-1.jpg`, `car-2.jpg`)  
   - For each image:  
     1. Extract LBP histograms over the same window size  
     2. Compute histogram intersection against each face‐descriptor and car‐descriptor  
     3. Compare the **maximum** face vs. car scores to label the image  
5. **Parameter Experiments**  
   - Repeat the above with different `window_size` values (e.g. 50, 80, 100) to see how window granularity affects descriptor quality and classification accuracy  
6. **Visualization**  
   - For each sliding window in `compute_LBP`, the notebook displays:  
     - The raw patch  
     - Its equalized version (`histogram_equalization`)  
     - The corresponding LBP histogram (bar plot)  

---

## File Structure

- `4 Texture Classification.ipynb`  
  The main notebook implementing LBP feature extraction, descriptor building, and classification.  
- `DatasetA/`  
  Contains sample grayscale images:  
  - Faces: `face-1.jpg`, `face-3.jpg`  
  - Cars: `car-1.jpg`, `car-2.jpg`, `car-3.jpg`  

---

## Requirements

- Python 3.6+  
- Dependencies:
  ```bash
  pip install opencv-python numpy matplotlib
