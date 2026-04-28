# Theory Questions - Week 1

## 1. What is a pixel, and what values can it hold in an 8-bit image?
A pixel is basically the smallest dot that makes up any digital image.  
For an 8-bit image, every pixel has a value from **0 to 255**.  

- 0 → pure black  
- 255 → pure white  
- Values in between → different shades of gray  

---

## 2. How is a grayscale image different from a color (RGB) image in terms of matrix representation?

The difference is in the "layers":

- **Grayscale:**
  - Represented as a **2D matrix** (rows × columns)
  - Each pixel has **one value** representing brightness  

- **Color (RGB):**
  - Represented as a **3D matrix**
  - Consists of **three 2D matrices**:
    - Red channel
    - Green channel
    - Blue channel  

---

## 3. What does the shape (480, 640, 3) mean for an image array?

This shape describes the image dimensions:

- **480** → height (number of rows)
- **640** → width (number of columns)
- **3** → number of color channels (Blue, Green, Red)

---

## 4. Why does OpenCV use BGR instead of RGB channel ordering?

This is mainly due to a **historical reason**:

- Early camera systems and libraries used **BGR format**
- OpenCV kept this format to maintain **compatibility with older systems**
- Even though RGB is more common today, BGR is still used internally in OpenCV  

---

## 5. How is matrix multiplication used in image transformations such as rotation?

In computer vision:

- Pixel positions are treated as **vectors**
- To rotate an image:
  - Each pixel location is multiplied by a **Rotation Matrix**

This transformation calculates the **new position of each pixel** after rotation.

---

## 6. What is the role of eigenvalues in computer vision applications?

Eigenvalues help identify the **important directions in data**.

They are used in:

- **Dimensionality Reduction (PCA):**
  - Keep the most important features
  - Reduce image size/data  

- **Feature Detection:**
  - Detect corners and edges
  - Analyze how pixel values change  

---

## 7. Explain the difference between `img[y, x]` and `img[x, y]` and why the ordering matters.

In Python/OpenCV, indexing follows **(row, column)**:

- `img[y, x]`
  - `y` → row (vertical axis)
  - `x` → column (horizontal axis)

- `img[x, y]`
  - Incorrect order
  - May give wrong values or errors  

### Why ordering matters:
- Image coordinates start from **top-left corner (0, 0)**
- `y` increases downward
- `x` increases to the right  

---

## 8. What is the range of pixel values for a 16-bit image?

A 16-bit image has a much larger range:

- Minimum value → **0**
- Maximum value → **65,535**

This allows:
- Higher precision
- Better image quality
- More intensity levels
