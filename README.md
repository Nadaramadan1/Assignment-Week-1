# Image Analysis & Filter Exploration

This project focuses on the fundamentals of **Digital Image Processing** and **Computer Vision**, exploring how images are represented as matrices and how linear algebra operations like **Convolution** are used to extract features.

---

## Learning Objectives

- Understand image representation (**Pixels, Intensity, Channels**)
- Perform matrix operations using **NumPy**
- Apply and compare spatial filters using **OpenCV**

---

## Built With

- **Python **
- **OpenCV** — Image loading and processing
- **NumPy** — Matrix operations
- **Matplotlib** — Visualization
- **Google Colab** 

---

## Image Processing Pipeline

This project analyzes three types of real-world images:

- **Portrait**
- **Landscape**
- **Document**

---

### 1. Matrix Representation

Each image is represented as a **3D NumPy array**.

For example:

- Resolution: $480 \times 640$
- Shape: `(480, 640, 3)`

Where:
- **480** → Height (rows)
- **640** → Width (columns)
- **3** → Color channels (BGR in OpenCV)

---

### 2. Convolution & Filtering

Five different filters were applied to analyze their effect:

- **Box Blur**
  - Simple averaging
  - Reduces noise

- **Gaussian Blur**
  - Weighted smoothing
  - Preserves natural details

- **Sobel X & Y**
  - Detect edges in horizontal and vertical directions

- **Laplacian**
  - Detects all edges (second-order derivative)

---

## Results & Analysis

| Image Type | Filtered Results 
|------------|------------------
| **Portrait** |(<img width="1110" height="765" alt="portrait results" src="https://github.com/user-attachments/assets/459f9b85-4b50-4df6-a295-df09afa2b965" />)
| **Landscape** |(<img width="1489" height="753" alt="lamdscape 2 results" src="https://github.com/user-attachments/assets/03603b25-5b80-4079-8dbb-9ebc50e8703a" />)
| **Document** |(<img width="1151" height="765" alt="document results" src="https://github.com/user-attachments/assets/64c85d1b-3035-4e10-9129-24d09483e9f8" />)
