## Image Compression via Block-wise SVD

## Overview

This project demonstrates image compression using **block-wise Singular Value Decomposition (SVD)**. The original grayscale image is divided into 8×8 blocks, and each block is compressed using only the top-𝑘 singular values for \( k \in \{1, 2, ..., 8\} \).

---

## Objectives

- Apply SVD to compress image blocks
- Analyze compression ratio, reconstruction error, and PSNR
- Visualize the trade-off between image quality and compression

---
## Key Files

- **`svd.ipynb`**  
  Contains source code, function definitions, metric calculations, graphs, and image comparisons.

- **`report.pdf`**  
  A polished PDF document containing:
  - Implementation summary
  - Important code snippets
  - Results table
  - Graphs and compressed image grid
  - Analytical insights

---

##  How It Works

1. The image is loaded and verified to be divisible by 8 (512×512).
2. Functions like `compress_block()` and `compress_image()` apply SVD and reconstruct blocks using top-k singular values.
3. Metrics such as **compression ratio**, **Frobenius norm error**, and **PSNR** are calculated for each k.
4. Results are visualized using:
   - Line plots of each metric vs. k
   - A 3×3 image grid showing original and compressed images with CR and PSNR.

---

##  Results Snapshot

| k  | Compression Ratio | Frobenius Error | PSNR (dB) |
|----|-------------------|-----------------|------------|
| 1  | 3.76              | 4288.71         | 34.13      |
| 4  | 0.94              | 765.69          | 44.68      |
| 8  | 0.47              | 0.00            | inf        |

> PSNR becomes infinite when the image is reconstructed exactly with all 8 singular values (k = 8).

---

## Conclusion

Block-wise SVD offers a scalable approach to image compression. By adjusting k, we can control the trade-off between compression efficiency and visual quality. This project demonstrates how SVD can be used for efficient low-rank approximations in practical applications.

---

##  Requirements

- Python 3.7+
- `numpy`, `matplotlib`, `PIL` (Pillow), `pandas`, `jupyter`

---
