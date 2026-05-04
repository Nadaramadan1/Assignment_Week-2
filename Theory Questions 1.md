
## Topic 3: Image Thresholding

### 1. What is the purpose of thresholding in image processing?
Thresholding is used to convert a grayscale image into a binary image to separate foreground objects from the background.

---

### 2. When would you prefer adaptive thresholding over global thresholding?
Adaptive thresholding is preferred when the image has uneven lighting, because it calculates a local threshold for each region instead of using a single global value.

---

### 3. Explain how Otsu's method determines the optimal threshold.
Otsu’s method automatically finds the optimal threshold by minimizing intra-class variance between foreground and background pixels.

---

### 4. What does THRESH_BINARY_INV do, and when would you use it?
THRESH_BINARY_INV inverts the binary output:
- Pixels above threshold → black  
- Pixels below threshold → white  

It is used when the foreground is darker than the background.

---

### 5. What kind of histogram does Otsu's method work best on?
Otsu’s method works best on bimodal histograms, where pixel values form two distinct peaks (foreground and background).
