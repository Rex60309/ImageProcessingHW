# ImageProcessHW

Implementing coursework for Image Processing.

## Requirements

- Python 3
- `numpy`, `opencv-python`, `matplotlib`, `scipy`, `pandas`

## Assignments

### HW1 — Ordered Dithering (`hw1/hw1.py`)
Applies two ordered dithering methods to a grayscale image:
- **Binary dithering** using a tiled 4×4 threshold matrix (`A_dithered_image.png`).
- **4-level extended dithering** using a tiled 2×2 matrix (`B_extended_dithered_image.png`).

### HW2 — Histogram Equalization (`hw2/hw2.py`)
Implements histogram equalization from scratch for both grayscale and color images:
- Computes the intensity histogram, cumulative distribution, and mapping table (exported as CSV).
- Enhances color images by scaling each RGB pixel by the ratio of equalized to original grayscale intensity (`G' / G`).
- Plots before/after images, grayscale cumulative histograms, and per-channel RGB histograms.

### HW3 — Spatial Filtering and Unsharp Masking (`hw3/hw3.py`)
Implements three spatial-domain operations on grayscale or color images with user-specified kernel size `n × n` and scale factor `k`:
- **Average filter** and **median filter** implemented from scratch (channel-by-channel for RGB).
- **Unsharp masking** using Gaussian blur to extract and add back high-frequency detail.

### HW4 — Image Rotation and Interpolation (`hw4/hw4.py`)
Generates a 200×200 synthetic square image and rotates it by `-30°` using SciPy's nearest-neighbor (`order=0`) and bilinear (`order=1`) interpolation. Plots both rotated images alongside an absolute pixel-difference heatmap.

### HW6 — Gaussian Noise Generation (`hw6/hw6.py`)
Generates zero-mean Gaussian noise (`var = 25`) using the Box–Muller transform, adds it to a uniform 256×256 grayscale image (gray level 100) with `[0, 255]` clipping, and plots the original/noisy images and their histograms.

### HW7 — Otsu's Thresholding (`hw7/hw7.py`)
Finds the optimal binary segmentation threshold by maximizing between-class variance across gray levels `1–255`, then displays the grayscale input, intensity histogram with the selected threshold, and binary output.

### HW9 — HSV Color Contrast Enhancement (`hw9/hw9.py`)
Implements `RGB ↔ HSV` color space conversion from scratch, equalizes only the `V` (value/brightness) channel, converts back to RGB, and displays the original and contrast-enhanced color images side by side.
