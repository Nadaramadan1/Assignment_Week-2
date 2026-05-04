## Theory Questions

### 1. Compare Global Thresholding, Adaptive Thresholding, and Otsu's Method. When should you use each?

*   **Global Thresholding:** Uses a single fixed threshold value for the entire image.
    *   **When to use:** Use it when the image has very uniform lighting and a clear contrast between foreground and background.
*   **Adaptive Thresholding:** Calculates different threshold values for small local regions of the image.
    *   **When to use:** Best for images with uneven lighting or shadows (like photos of documents taken with a phone).
*   **Otsu's Method:** Automatically determines the optimal threshold by analyzing the image histogram.
    *   **When to use:** Best for bimodal images (images with two distinct peaks in their histogram) when you want the threshold to be calculated automatically.

---

### 2. What is Erosion? Give a practical use case.

**Erosion** is a morphological operation that "erodes" or shrinks the boundaries of foreground (white) objects[cite: 1]. It works by removing pixels at the edges of objects based on a structuring element.
*   **Practical Use Case:** It is commonly used to remove small white noise (salt noise) from the background or to separate two connected objects.

---

### 3. Explain CLAHE and why it's better than Global Histogram Equalization.

*   **Global Histogram Equalization:** Enhances the contrast of the entire image at once. However, it can over-amplify noise in relatively uniform areas or "burn" the highlights.
*   **CLAHE (Contrast Limited Adaptive Histogram Equalization):** Operates on small tiles (blocks) of the image rather than the whole image[cite: 1]. It also limits the contrast enhancement to prevent noise over-amplification.
*   **Why it's better:** It provides much better local contrast enhancement and preserves details in both dark and bright areas without distorting the overall image.

---

### 4. Describe a full preprocessing pipeline for a noisy, low-contrast binary document image.

To transform a noisy, low-contrast document into a clean binary image, the following pipeline is used:
1.  **Grayscale Conversion:** Convert the image to 8-bit grayscale to focus on intensity rather than color.
2.  **CLAHE:** Apply local contrast enhancement to make the text stand out from the background.
3.  **Gaussian Blur:** Apply a light blur to reduce high-frequency noise and smooth the edges.
4.  **Adaptive Thresholding:** Convert to a binary image using local thresholds to handle any remaining shadows or uneven lighting.
5.  **Morphological Opening:** Apply erosion followed by dilation to remove small noise particles and clean up the text strokes.
