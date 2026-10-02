# Lab 5 — Spatial Filtering: Smoothing & Sharpening

Applying spatial filters (low-pass and high-pass) to images using OpenCV, on `skimage.data.astronaut()`.

## Tasks
| Task | Description | Function |
|---|---|---|
| Task 1 | Unsharp masking (sigma=2, amount=1.5) | `cv2.GaussianBlur` |
| Assessment 1 | 7×7 box filter with a manual kernel | `cv2.filter2D` |
| Assessment 2 | 5×5 vs 21×21 Gaussian blur | `cv2.GaussianBlur` |
| Assessment 3 | 3×3 Laplacian sharpening (original − laplacian) | `cv2.Laplacian` |
| Q1 | Box filters: 3×3, 9×9, 15×15 | `cv2.blur` |
| Q2 | Median vs Gaussian on salt-and-pepper noise | `cv2.medianBlur` |
| Q3 | Bilateral vs Gaussian (edge preservation) | `cv2.bilateralFilter` |

## Key Findings
- Larger kernels give stronger blur and lose more detail
- Gaussian blur looks smoother than box (no blocky artifacts)
- Median removes salt-and-pepper noise; Gaussian only smears it
- Bilateral smooths flat areas while keeping edges sharp
- Laplacian and unsharp masking enhance edges

## Run
Open `Lab5_Spatial_Filtering.ipynb` in Jupyter or Colab and run all cells.
