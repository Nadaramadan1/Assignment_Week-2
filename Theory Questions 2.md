## Topic 2: Morphological Operations

### 1. What is a structuring element?
A structuring element is a small matrix (kernel) used to probe and process shapes in a binary image during morphological operations.

---

### 2. Explain erosion vs dilation (visual idea)
- **Erosion:** Shrinks white regions by removing boundary pixels.  
- **Dilation:** Expands white regions by adding pixels to boundaries.

Example:
- Erosion → removes small dots/noise  
- Dilation → fills small gaps and enlarges objects  

---

### 3. When would you use Opening vs Closing?
- **Opening (Erosion → Dilation):** Used to remove small noise from the background while preserving object shape.  
- **Closing (Dilation → Erosion):** Used to fill small holes inside objects.

---

### 4. How does morphological gradient relate to edge detection?
Morphological gradient calculates the difference between dilation and erosion, highlighting the boundaries of objects. It is used for edge detection in binary images.

---

### 5. What happens if you apply dilation many times?
Repeated dilation causes white regions to continuously expand, which may lead to merging of objects and loss of fine details.

---
