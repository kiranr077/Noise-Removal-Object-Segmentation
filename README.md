# Noise-Removal-Object-Segmentation
Digital Image Processing project for noise removal and object segmentation
# Noise Removal and Object Segmentation Using Digital Image Processing

## About the Project

This project demonstrates noise removal and object segmentation using Digital Image Processing techniques.

In this project, an image from the Oxford-IIIT Pet Dataset is converted into grayscale. Gaussian noise and Salt-and-Pepper noise are added to the image. Mean and Median filters are then used to reduce the noise.

After noise removal, Otsu's thresholding method and morphological operations are used for object segmentation. Canny edge detection is also applied to identify the edges of the object.

The performance of image restoration is measured using MSE, PSNR and SSIM. The segmentation performance is measured using IoU and Dice Score.

## Objectives

- Convert RGB images into grayscale images.
- Add Gaussian noise to the image.
- Add Salt-and-Pepper noise to the image.
- Apply 7 × 7 Mean filtering.
- Apply 7 × 7 Median filtering.
- Evaluate restoration using MSE, PSNR and SSIM.
- Perform image segmentation using Otsu's thresholding.
- Apply morphological opening and closing.
- Evaluate segmentation using IoU and Dice Score.
- Perform Canny edge detection.
- Evaluate the complete process on multiple images.

## Dataset

The project uses the Oxford-IIIT Pet Dataset.

The dataset contains images of cats and dogs along with their segmentation masks.

- Total images: 3680
- Image type: RGB
- Segmentation masks: Available
- Dataset used for: Image restoration and object segmentation

## Methodology

The project follows these steps:

Original Image
↓
Grayscale Conversion
↓
Add Gaussian and Salt-and-Pepper Noise
↓
Mean and Median Filtering
↓
MSE, PSNR and SSIM Evaluation
↓
Otsu Thresholding
↓
Morphological Processing
↓
Object Segmentation
↓
IoU and Dice Evaluation
↓
Canny Edge Detection

## Techniques Used

### 1. Grayscale Conversion

The original RGB image is converted into a grayscale image using OpenCV.

### 2. Gaussian Noise

Gaussian noise is added to the grayscale image using:

- Mean = 0
- Sigma = 25

### 3. Salt-and-Pepper Noise

Salt-and-Pepper noise is added to the grayscale image with a noise amount of 5%.

### 4. Mean Filtering

A 7 × 7 Mean filter is applied to reduce noise from the image.

### 5. Median Filtering

A 7 × 7 Median filter is applied to reduce noise, especially Salt-and-Pepper noise.

### 6. Restoration Evaluation

The restored images are evaluated using:

- Mean Squared Error (MSE)
- Peak Signal-to-Noise Ratio (PSNR)
- Structural Similarity Index (SSIM)

### 7. Otsu Thresholding

Otsu's thresholding method is used to automatically find an optimal threshold and separate the foreground from the background.

### 8. Morphological Processing

Morphological Opening and Closing operations are applied using a 5 × 5 kernel.

Opening helps remove small unwanted regions, while Closing helps fill small gaps.

### 9. IoU and Dice Score

The segmented image is compared with the ground-truth segmentation mask using:

- Intersection over Union (IoU)
- Dice Score

### 10. Canny Edge Detection

Canny edge detection is applied to identify important edges and boundaries in the image.

## Results

### Restoration Results for the Selected Image

| Method | MSE | PSNR | SSIM |
|---|---:|---:|---:|
| Gaussian + Mean | 226.61 | 24.58 dB | 0.6741 |
| Gaussian + Median | 192.09 | 25.30 dB | 0.6623 |
| Salt-and-Pepper + Mean | 315.39 | 23.14 dB | 0.5729 |
| Salt-and-Pepper + Median | 164.73 | 25.96 dB | 0.7452 |

### Segmentation Results for the Selected Image

- Otsu Threshold: 144
- IoU: 0.1077
- Dice Score: 0.1944

### Average Results on 20 Images

| Metric | Average Result |
|---|---:|
| MSE | 101.66 |
| PSNR | 29.03 dB |
| SSIM | 0.7979 |
| IoU | 0.2456 |
| Dice Score | 0.3575 |

## Technologies Used

- Python
- Google Colab
- OpenCV
- NumPy
- Matplotlib
- Scikit-image
- Torchvision

## Project Structure

```text
Noise-Removal-Object-Segmentation/
│
├── README.md
├── source_code.py
├── final report.docx
│
└── screenshots/
    ├── original_ground_truth.png
    ├── gaussian_noise.png
    ├── salt_pepper_noise.png
    ├── filtering.png
    ├── restoration_metrics.png
    ├── otsu.png
    ├── morphology.png
    ├── canny.png
    ├── final_output.png
    └── final_graphs.png
