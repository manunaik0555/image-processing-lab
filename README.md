# # Image Processing and Histogram Analysis in Python

This repository contains a collection of Python scripts and Jupyter Notebook examples demonstrating essential image processing workflows using `scikit-image`, `NumPy`, and `Matplotlib`.

## Table of Contents
- [Introduction](#introduction)
- [Features & Modules](#features--modules)
  - [1. Channel Isolation (RGB)](#1-channel-isolation-rgb)
  - [2. Color Space Conversions (HSV & LAB)](#2-color-space-conversions-hsv--lab)
  - [3. Pseudocolor / Colormap Mapping](#3-pseudocolor--colormap-mapping)
  - [4. RGB Histogram Visualization](#4-rgb-histogram-visualization)
  - [5. Histogram Intersection (Similarity Analysis)](#5-histogram-intersection-similarity-analysis)
  - [6. Histogram Equalization](#6-histogram-equalization)
- [Requirements](#requirements)
- [Getting Started](#getting-started)

---

## Introduction
Understanding and manipulating digital image structures, color representation profiles, and intensity distributions are fundamental concepts in computer vision. This project provides clean, educational code blocks that walk through basic extraction, transformation, visualization, and normalization procedures.

## Features & Modules

### 1. Channel Isolation (RGB)
Extracts individual color channels (Red, Green, and Blue) from an RGB image. It showcases two approaches:
- Isolating a channel physically by zeroing out the remaining color matrices.
- Extracting the channel as a single-channel grayscale representation displayed with specialized color limits.

### 2. Color Space Conversions (HSV & LAB)
Converts RGB data into specialized spaces designed for distinct computer vision requirements:
- **HSV (Hue, Saturation, Value):** Separates chromatic information (Hue) from purity (Saturation) and brightness (Value).
- **CIE L*a*b*:** Separates perceived luminance ($L$) from color opponent dimensions ($a$ and $b$), modeling human visual perception.

### 3. Pseudocolor / Colormap Mapping
Applies divergent scientific colormaps (such as `hot`, `jet`, `hsv`, `terrain`, `bone`, and `copper`) onto single-channel grayscale arrays to expose subtle intensity gradients.

### 4. RGB Histogram Visualization
Generates multi-line cumulative intensity distribution step-plots for R, G, and B components, allowing quick profiling of image contrast, brightness, and color casts.

### 5. Histogram Intersection (Similarity Analysis)
Implements a normalized histogram intersection algorithm to quantitatively measure visual similarity between different image domains, including robustness checking against image transformations (such as rotation).

$$\text{Intersection}(H_1, H_2) = \frac{\sum \min(H_1(i), H_2(i))}{\sum H_2(i)}$$

### 6. Histogram Equalization
Enhances structural contrast using global histogram stretching. Demonstrates:
- Independent channel-by-channel RGB equalization.
- Contrast enhancement limited strictly to the Value ($V$) channel in HSV space to preserve original chromaticity without color distortion.

---

## Requirements
To run the notebook, install the following scientific computing libraries:

```bash
pip install numpy matplotlib scikit-image
```

## Getting Started
Clone this repository and open the Jupyter Notebook:

```bash
git clone https://github.com/your-username/image-histogram-analysis.git
cd image-histogram-analysis
jupyter notebook
```
