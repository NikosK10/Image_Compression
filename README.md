# Laplacian Pyramid Image Compression

This project is an implementation of the Laplacian Pyramid coding scheme as described in the paper:  
**"The Laplacian Pyramid as a Compact Image Code"** by Burt and Adelson (IEEE, 1983).

## Overview

This notebook demonstrates how to encode and reconstruct images using a Laplacian pyramid structure, which is a multi-resolution representation for image compression. The method combines aspects of both predictive and transform coding techniques to achieve efficient data representation and compression.

## What This Project Does

- **Gaussian Pyramid Construction**: The original image is successively downsampled and low-pass filtered to form a pyramid of increasingly blurred and smaller images.
- **Laplacian Pyramid Generation**: Each level of the Laplacian pyramid is obtained by subtracting an expanded version of the next higher level of the Gaussian pyramid from the current level.
- **Image Encoding**: Only the difference images (Laplacian levels) and the smallest Gaussian level are stored, reducing data redundancy.
- **Quantization**: Each Laplacian level is quantized to further compress the data by reducing precision where human visual sensitivity is lower.
- **Image Reconstruction**: The original image is reconstructed by reversing the pyramid process—expanding and summing the Laplacian levels.

## Key Features

- Implementation closely follows the original algorithm and design decisions from the paper.
- Includes visualizations of the Gaussian and Laplacian pyramids at each step.
- Demonstrates quantization and evaluates reconstruction quality.
- Suitable for progressive transmission: higher levels (low-res) are transmitted first for quick previews.

## Files

- `Image_Video_LAB1_03121868_Katsaidonis_Nikolaos.ipynb`: Main implementation notebook.
- `paper_laplacian_pyramid.pdf`: Reference paper.

## Requirements

- Python 3.x
- Libraries: `NumPy`, `Matplotlib`, `OpenCV` (or `PIL`), `SciPy`

## How to Use

1. Open the notebook in Jupyter.
2. Load an image and run all cells to see the full pipeline: from pyramid construction to image reconstruction.
3. You can adjust the number of pyramid levels and quantization steps to observe their effect on compression quality.

## Author

Nikolaos Katsaidonis  
Lab Assignment for Image & Video Processing
