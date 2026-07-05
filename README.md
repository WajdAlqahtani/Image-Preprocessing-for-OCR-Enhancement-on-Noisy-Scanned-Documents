# Document Image Preprocessing for OCR Enhancement

## Overview
This project evaluates different image preprocessing techniques for improving Optical Character Recognition (OCR) performance on noisy scanned documents. The goal is to enhance document readability while preserving image structure and text details.

## Problem
OCR systems often perform poorly on scanned documents affected by noise, low contrast, blur, and illumination variations. Poor image quality can reduce text readability and lead to inaccurate recognition results. This project explores preprocessing pipelines that improve OCR performance before applying OCR engines.

## Dataset
The project uses the FUNSD+ dataset, which contains noisy scanned document images. The dataset includes real-world document issues such as scanning artifacts, low contrast, blur, and illumination variations.

## Methodology
The project compares multiple preprocessing pipelines and evaluates their effect on OCR performance and image quality.

Main steps:
1. Load scanned document images
2. Apply preprocessing techniques
3. Evaluate processed images using image quality metrics
4. Apply OCR using Tesseract and EasyOCR
5. Compare OCR performance before and after preprocessing

## Preprocessing Techniques
The tested preprocessing techniques include:

- Grayscale conversion
- Image resizing using interpolation
- CLAHE contrast enhancement
- Median filtering
- Sharpening
- Otsu thresholding
- Adaptive thresholding
- Morphological operations

## OCR Engines
The project uses:

- Tesseract OCR
- EasyOCR

## Evaluation Metrics
The project evaluates performance using:

- OCR Confidence
- Detected Words
- PSNR
- SSIM
- Processing Time

## Results
The selected Tesseract preprocessing pipeline improved OCR performance:

| Metric | Before | After | Change |
|---|---:|---:|---:|
| OCR Confidence | 62.00 | 63.75 | +2.82% |
| Words Detected | 159.02 | 164.48 | +3.43% |

The image quality metrics remained high, with SSIM around 0.988 and PSNR around 30.4, showing that the preprocessing preserved document structure while improving OCR readability.

## Key Finding
The results showed that more preprocessing steps do not always improve OCR performance. Simpler pipelines often performed better because they preserved text structure and avoided damaging character boundaries.

## Technologies Used
- Python
- OpenCV
- NumPy
- Pandas
- Matplotlib
- scikit-image
- Tesseract OCR
- EasyOCR
- Hugging Face Datasets

## Future Work
- Test additional OCR engines
- Evaluate deep learning-based OCR models
- Try advanced denoising and super-resolution methods
- Test the pipeline on larger and more diverse document datasets