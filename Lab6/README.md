# Lab 6: Frequency Domain Filtering (Sobel)

Apply the Sobel edge-detection filters in the frequency domain instead of using spatial convolution.

## Method
1. Load the cameraman image and resize it to 256×256.
2. Pad each 3×3 Sobel kernel to the image size, placing it at the center.
3. Apply `ifftshift` to move the kernel center to (0,0), then `fft2` to get its frequency response.
4. Compute `fft2` of the image and multiply it pointwise by each filter.
5. Apply `ifft2` and take the real part to get the filtered image.
6. Combine both directions: `magnitude = sqrt(Gx² + Gy²)`.

## Results
- **Sobel X** highlights vertical edges.
- **Sobel Y** highlights horizontal edges.
- **Magnitude** shows the full edge map.
- Sobel is a high-pass filter, so low frequencies (the center of the shifted spectrum) are suppressed.
- The result matches spatial convolution with circular boundaries (max difference ≈ 1e-15).

## Conclusion
Convolution in the spatial domain equals multiplication in the frequency domain. Both give the same result, but the frequency approach makes the filter's behavior easy to see.
