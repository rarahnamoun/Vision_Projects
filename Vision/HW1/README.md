# Computer Vision HW1 - Text Extraction & Star Counting

## Overview
This homework assignment covers fundamental computer vision techniques for text extraction and object detection/counting.

## Project Structure
```
HW1/
├── src/
│   └── HW1_Vision_RashinRahnamoun_400243092.ipynb  # Main implementation
└── report.pdf                                     # Assignment report
```

## Assignment Questions

### Question 1: License Plate Text Extraction
- **Objective**: Extract text from a car license plate using OCR techniques
- **Technologies Used**:
  - EasyOCR for optical character recognition
  - OpenCV for image preprocessing
  - Tesseract OCR as alternative approach
- **Key Techniques**:
  - Image preprocessing and region of interest (ROI) selection
  - Grayscale conversion and thresholding
  - Text extraction with character allowlisting
  - Multiple OCR engine comparison

### Question 2: Star Counting in Night Sky Images
- **Objective**: Count stars in astronomical images
- **Technologies Used**:
  - OpenCV for image processing
  - Morphological operations
  - Contour detection and analysis
- **Key Techniques**:
  - Image preprocessing (grayscale conversion, noise reduction)
  - Threshold-based star detection
  - Morphological operations for noise removal
  - Contour analysis for star counting
  - Parameter tuning for accurate detection

## Implementation Highlights

### Text Extraction Pipeline
1. **Image Loading and Preprocessing**
   - Load car image with license plate
   - Define Region of Interest (ROI) for license plate area
   - Convert to grayscale for better OCR performance

2. **OCR Processing**
   - Apply Otsu's thresholding for binary conversion
   - Use EasyOCR with English language model
   - Apply character allowlist for license plate format
   - Extract and display results

### Star Counting Pipeline
1. **Image Preprocessing**
   - Load night sky image
   - Convert to grayscale
   - Apply Gaussian blur for noise reduction

2. **Star Detection**
   - Apply binary thresholding
   - Use morphological operations (opening/closing)
   - Find contours representing stars
   - Filter contours by area and circularity
   - Count valid star detections

## Key Learning Outcomes
- **OCR Techniques**: Understanding of optical character recognition methods
- **Image Preprocessing**: Mastery of fundamental image processing operations
- **Morphological Operations**: Application of mathematical morphology for noise reduction
- **Contour Analysis**: Object detection and counting using contour properties
- **Parameter Tuning**: Optimization of algorithm parameters for specific tasks

## Dependencies
- OpenCV (cv2)
- EasyOCR
- Tesseract OCR
- Matplotlib
- NumPy

## Usage
1. Open the Jupyter notebook in Google Colab or local environment
2. Install required dependencies
3. Upload test images (car.jpg for Q1, night sky image for Q2)
4. Run cells sequentially to execute the complete pipeline
5. Observe results and extracted text/star counts

## Results
The implementation successfully:
- Extracts text from license plates with high accuracy
- Counts stars in astronomical images with configurable precision
- Demonstrates robustness across different image qualities
- Provides visualizations of intermediate processing steps