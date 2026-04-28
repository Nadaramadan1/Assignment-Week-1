# Theory Section - Assignment 1

## 1. What is a pixel? Explain intensity values for 8-bit images.

A **pixel** (short for Picture Element) is the smallest unit in a digital image.  
It represents a single point that holds a specific color or intensity value.

For **8-bit images**:
- Each pixel is stored using **8 bits**
- This allows **2⁸ = 256** possible values

### Range:
- **0** → Pure Black
- **255** → Pure White
- Values in between → Shades of gray (or intensity levels)

---

## 2. What is the shape of a color image with H=480, W=640? Explain each dimension.

The shape of the image is:

**(480, 640, 3)**

### Explanation:
- **480 (Height):** Number of rows (top → bottom)
- **640 (Width):** Number of columns (left → right)
- **3 (Channels):** Color channels:
  - Red
  - Green
  - Blue

> Note: In OpenCV, the channel order is **BGR** (Blue, Green, Red)

---

## 3. Explain convolution step by step. Include kernel, sliding window, and output.

Convolution is a technique used to apply a filter to an image.

### Steps:

1. **Kernel (Filter):**
   - A small matrix (e.g., 3×3) containing weights

2. **Sliding Window:**
   - Place the kernel on the image (starting from top-left)

3. **Element-wise Multiplication:**
   - Multiply each kernel value with the corresponding pixel value

4. **Summation:**
   - Add all the results together

5. **Output Pixel:**
   - The result becomes one pixel in the output image (feature map)

6. **Repeat:**
   - Move the kernel across the image until all regions are processed

---

## 4. Compare Box Blur vs Gaussian Blur vs Sobel — purpose and kernel differences.

| Filter | Purpose | Kernel Characteristics |
|--------|--------|------------------------|
| **Box Blur** | Simple smoothing and noise reduction | All kernel values are equal (e.g., 1/9). Treats all neighbors equally |
| **Gaussian Blur** | Smooth and natural blurring | Kernel values follow a Gaussian distribution. Center has higher weight |
| **Sobel** | Edge detection | Uses gradient values (e.g., -1, 0, 1). Detects intensity changes |
