## Topic 3: Histogram Equalization & Gamma Correction

### 1. What does a histogram of a low-contrast image look like?
A low-contrast image has a histogram where pixel values are concentrated in a narrow range, usually in the middle of the intensity scale.  
This means the image does not use the full range (0–255), making it look dull and lacking clear differences between light and dark regions.

---

### 2. How does histogram equalization improve image quality?
Histogram equalization improves image quality by redistributing pixel intensity values across the full range (0–255).  
This increases contrast by making dark regions darker and bright regions brighter, revealing hidden details in the image.

---

### 3. What is the difference between global histogram equalization and CLAHE?
- **Global Histogram Equalization:** Applies a single transformation to the entire image. It may improve contrast but can also amplify noise.

- **CLAHE (Contrast Limited Adaptive Histogram Equalization):** Works on small regions (tiles) and applies local contrast enhancement while limiting noise amplification.

CLAHE is more suitable for real-world images with uneven lighting.

---

### 4. If γ = 0.5, does the image get brighter or darker? Why?
The image becomes brighter because when γ < 1, the transformation boosts lower intensity values, making dark regions lighter.

---

### 5. When would you use CLAHE over standard histogram equalization?
CLAHE is used when the image has:
- Uneven lighting conditions  
- Low contrast with important local details  
- Need to avoid noise amplification  

---
