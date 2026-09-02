# Lab 2 — Digital Image Fundamentals

Covers: sampling & quantization, arithmetic ops, and set/logical ops on grayscale images. Uses built-in `skimage` images, so it runs with no external files.

## Requirements
`pip install numpy opencv-python pillow scikit-image matplotlib`

## Run
Open `Lab2_Digital_Image_Fundamentals_2_solved.ipynb` and Run All (in order — later cells reuse variables from earlier sections).

## Tasks
- **1a/1b:** vary sampling factor and quantization levels, observe the effect.
- **2a:** subtract two images.
- **2b:** add constant 175 (brightening).
- **2c–2e:** intersection `A & B`, set difference `A & ~B`, symmetric difference `A ^ B`.

## Note
Arithmetic is on `uint8`, so add/subtract may wrap around (matches the lab style).
