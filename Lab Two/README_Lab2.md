# Lab 2: Digital Image Fundamentals

**Course:** ARTI407 – Image Processing  
**College:** College of Computer Science and Information Technology  
**University:** Imam Abdulrahman Bin Faisal University  

---

## Overview

This lab introduces the fundamental concepts of digital image processing, focusing on:

- Image Sampling
- Image Quantization
- Arithmetic Operations
- Logical / Set Operations

The lab is implemented in Python using OpenCV, NumPy, Pillow, scikit-image, and Matplotlib.

The notebook uses built-in images from `skimage.data`, so no external image files are required.

---

## Objectives

By completing this lab, we learn how to:

- Perform image sampling to change spatial resolution.
- Perform image quantization to change intensity resolution.
- Observe the effect of different sampling factors.
- Observe the effect of different quantization levels.
- Apply arithmetic operations to grayscale images.
- Add a constant value to an image.
- Apply logical operations between images.
- Display and compare image-processing results.

---

## Libraries Used

```python
import cv2
import numpy as np
from PIL import Image
from skimage import data
import matplotlib.pyplot as plt
```

---

## Lab Tasks

### Task 1: Image Sampling

Sampling changes the spatial resolution of an image by reducing the number of pixels.

The following sampling factors are tested:

```text
1, 2, 4, 8, 16
```

As the sampling factor increases, the image contains fewer pixels and loses spatial detail.

---

### Task 2: Image Quantization

Quantization changes the intensity resolution of the image by reducing the number of grayscale levels.

The following quantization levels are tested:

```text
2, 4, 8, 16, 64, 256
```

Using fewer quantization levels results in fewer available intensity values and more visible intensity steps.

---

### Task 3: Image Subtraction

Two grayscale images are resized to the same dimensions and subtracted from each other.

Pixel values are clipped to the valid grayscale range:

```text
0 - 255
```

---

### Task 4: Add a Constant Value

A constant value of:

```text
175
```

is added to the image.

The result is clipped to ensure that pixel values remain between `0` and `255`.

---

### Task 5: Set Difference

Set difference is performed using a bitwise operation:

```python
A & ~B
```

---

### Task 6: Symmetric Difference

Symmetric difference is performed using:

```python
A ^ B
```

---

### Task 7: Intersection

Intersection between two images is performed using:

```python
A & B
```

---

### Additional Operation: Union

Union is performed using:

```python
A | B
```

---

## Logical Operations Summary

| Operation | Expression |
|---|---|
| Intersection | `A & B` |
| Set Difference | `A & ~B` |
| Symmetric Difference | `A ^ B` |
| Union | `A \| B` |

---

## Key Observations

- Increasing the sampling factor decreases spatial resolution.
- Decreasing quantization levels decreases intensity resolution.
- Arithmetic operations may cause overflow or underflow if pixel values are not handled correctly.
- Pixel values should remain within the grayscale range of `0–255`.
- Logical operations combine images using bitwise relationships between pixel values.

---

## How to Run

1. Open the notebook:

   ```text
   Lab2_Digital_Image_Fundamentals_solved(1).ipynb
   ```

2. Run it using:

   - Jupyter Notebook
   - JupyterLab
   - Google Colab

3. Install the required libraries if needed:

   ```bash
   pip install numpy opencv-python pillow scikit-image matplotlib
   ```

4. Run all notebook cells in order.

5. Observe and compare the output images.

---

## Conclusion

This lab demonstrates important digital image fundamentals through sampling, quantization, arithmetic operations, and logical operations.

The experiments show how changing spatial resolution, intensity resolution, and pixel values affects the visual appearance and information contained in a digital image.
