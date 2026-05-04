<div align="center">

# AI Document Scanner
### Phase 1: Foundation - Week 2 Assignment @ Star Union

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white)
![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)

## Author
**Nada Shams Eldin**  


</div>

---

## Overview
This project focuses on building an advanced **Image Preprocessing Pipeline** designed to transform low-quality, noisy, and unevenly lit document scans into clean, high-contrast, OCR-ready images.

### Key Features
*   **Contrast Enhancement:** Using CLAHE to handle uneven lighting.
*   **Smart Segmentation:** Adaptive Thresholding to isolate text from complex backgrounds.
*   **Noise Removal:** Gaussian Denoising & Morphological cleaning.
*   **Real-time Ready:** Implemented as a Streamlit Web App for interactive testing.

---

## The Preprocessing Pipeline
The core logic follows a structured Computer Vision pipeline to ensure maximum text clarity:

1.  **Grayscale Conversion:** Simplifies image data by focusing on intensity.
2.  **CLAHE (Contrast Limited Adaptive Histogram Equalization):** Enhances local contrast without over-amplifying noise—crucial for document shadows.
3.  **Gaussian Blur:** Smooths the image to remove high-frequency noise.
4.  **Adaptive Thresholding:** Dynamically calculates local thresholds to separate text from background, effectively handling harsh shadows.
5.  **Morphological Operations (Opening & Closing):** Removes small particles and fills gaps in text characters to ensure structural integrity.

---

## Visual Results
| Original (Grayscale) | Final Scanned Output |
| :---: | :---: |
| (<img width="640" height="853" alt="micah-boswell-00nHr1Lpq6w-unsplash" src="https://github.com/user-attachments/assets/f62c4c57-0d1b-4787-99f4-07a659dad93e" />) | (<img width="640" height="853" alt="clean_micah-boswell-00nHr1Lpq6w-unsplash (1)" src="https://github.com/user-attachments/assets/f7180ab0-b430-4d9e-874a-86abaecebdaf" />) |


---
