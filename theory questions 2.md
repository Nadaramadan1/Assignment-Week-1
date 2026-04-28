# Theory Questions - Part 2

## 1. Define convolution in your own words. How is it different from simple multiplication?

Convolution is the process of sliding a small matrix (called a kernel) over an image.  
At each position, we multiply corresponding values and sum them to produce a new pixel value.

**Difference:**
- **Simple multiplication:** multiplies two numbers directly
- **Convolution:** combines two datasets (image + kernel) to capture spatial relationships

---

## 2. What is a kernel/filter? Give two examples and explain what each one detects.

A kernel (or filter) is a small matrix (e.g., 3×3) used to extract features from an image.

- **Sobel Filter:**
  - Detects edges
  - Highlights areas with strong intensity changes

- **Gaussian Filter:**
  - Blurs the image
  - Reduces noise by averaging nearby pixel values

---

## 3. What is the difference between SAME and VALID padding?

- **VALID Padding:**
  - No padding is added
  - Output size is smaller than input

- **SAME Padding:**
  - Padding (usually zeros) is added around the image
  - Output size remains the same as input

---

## 4. If you convolve a 100x100 image with a 3x3 kernel (no padding, stride=1), what is the output size?

Using the formula:

Output size = (Input - Kernel + 1)

- Height = 100 - 3 + 1 = 98  
- Width = 100 - 3 + 1 = 98  

**Final output:** 98 × 98

---

## 5. Why does a Sobel X filter detect vertical edges?

The Sobel X filter detects changes in the **horizontal direction (along the x-axis)**.  

Vertical edges are formed where pixel values change from left to right, so the filter highlights these boundaries.

---

## 6. What happens when all kernel values are identical (e.g., all = 1/9)?

This creates a **Box Blur**:

- Takes the average of the surrounding pixels
- Replaces the center pixel with this average
- Produces a smoothing (blurring) effect

---

## 7. How does stride affect the size of the output feature map?

Stride is the step size of the kernel:

- **Stride = 1:** moves pixel by pixel → larger output
- **Stride = 2:** skips pixels → smaller output

Increasing stride reduces the output size (downsampling).

---

## 8. Why does CNN learn kernels automatically during training?

CNNs learn kernels using **backpropagation**:

- Instead of manually designing filters
- The model adjusts kernel values automatically
- Learns optimal features for the task (e.g., edges, shapes, objects)

This makes CNNs more flexible and powerful.
