# Computer Vision HW2 - Deep Learning Applications

## Overview
This homework assignment explores advanced deep learning techniques in computer vision, covering image classification, image quality assessment, and image denoising using neural networks.

## Project Structure
```
HW2/
├── Q1/
│   └── HW2_Vision_Q1(1).ipynb        # Shoe classification with CNNs
├── Q2/
│   └── Vision_HW2_Q2(2).ipynb        # Image quality assessment
├── Q3/
│   ├── HW2_Vision_Q3_2.ipynb         # Airplane detection and segmentation
│   └── HW2_Vision_Q3(1).ipynb        # Alternative implementation
└── report.pdf                        # Complete assignment report
```

## Assignment Questions

### Question 1: Shoe Classification using Convolutional Neural Networks
**File**: `Q1/HW2_Vision_Q1(1).ipynb`

- **Objective**: Build and train CNN models for shoe type classification
- **Dataset**: Custom shoe dataset with multiple categories
- **Technologies Used**:
  - TensorFlow/Keras for deep learning
  - Custom CNN architectures
  - Transfer learning approaches
  - FastAI for advanced implementations

**Key Techniques**:
- Multi-layer CNN architecture design
- Data augmentation and preprocessing
- Transfer learning with pre-trained models
- Performance evaluation and visualization
- Model comparison and optimization

### Question 2: Image Quality Assessment
**File**: `Q2/Vision_HW2_Q2(2).ipynb`

- **Objective**: Implement and compare image quality metrics
- **Technologies Used**:
  - OpenCV for image processing
  - BRISQUE (Blind/Referenceless Image Spatial Quality Evaluator)
  - PIQE (Perception based Image Quality Evaluator)
  - Custom quality assessment algorithms

**Key Techniques**:
- No-reference image quality assessment
- Statistical feature extraction
- Perceptual quality metrics implementation
- Comparative analysis of quality metrics
- Visualization of quality assessments

### Question 3: Airplane Detection and Segmentation
**Files**: `Q3/HW2_Vision_Q3_2.ipynb`, `Q3/HW2_Vision_Q3(1).ipynb`

- **Objective**: Detect and segment airplanes in images using deep learning
- **Dataset**: Airplane dataset with annotations
- **Technologies Used**:
  - PyTorch for deep learning
  - U-Net architecture for segmentation
  - Object detection frameworks
  - Advanced data preprocessing

**Key Techniques**:
- Object detection pipeline implementation
- Semantic segmentation using U-Net
- Data augmentation for object detection
- Performance metrics (IoU, mAP)
- Visualization of detection results

## Implementation Highlights

### CNN Architecture Design
- **Convolutional Layers**: Feature extraction with multiple filter sizes
- **Pooling Layers**: Spatial dimension reduction
- **Fully Connected Layers**: Classification head design
- **Regularization**: Dropout and batch normalization
- **Activation Functions**: ReLU, softmax for multi-class classification

### Transfer Learning Implementation
- Pre-trained model adaptation
- Fine-tuning strategies
- Feature extraction vs full training
- Performance comparison with custom architectures

### Image Quality Assessment Pipeline
1. **Preprocessing**: Image normalization and format conversion
2. **Feature Extraction**: Statistical and perceptual features
3. **Quality Scoring**: BRISQUE and PIQE implementation
4. **Evaluation**: Quality score interpretation and validation

### U-Net Segmentation Architecture
- **Encoder Path**: Downsampling with feature extraction
- **Decoder Path**: Upsampling with skip connections
- **Skip Connections**: Feature map concatenation
- **Output Layer**: Pixel-wise classification
- **Loss Function**: Dice loss and binary cross-entropy

## Key Learning Outcomes
- **Deep Learning Fundamentals**: CNN architecture design and training
- **Transfer Learning**: Leveraging pre-trained models effectively
- **Image Quality Assessment**: Understanding perceptual quality metrics
- **Semantic Segmentation**: Pixel-level classification techniques
- **Object Detection**: Localization and classification combined
- **Performance Evaluation**: Metrics for classification and segmentation tasks
- **Data Augmentation**: Improving model generalization

## Dependencies
- TensorFlow/Keras
- PyTorch
- OpenCV (cv2)
- NumPy
- Matplotlib
- Scikit-learn
- Seaborn
- PIL (Pillow)
- BRISQUE
- PIQE
- FastAI
- Visualkeras
- Torchsummary

## Usage Instructions

### Q1 - Shoe Classification
1. Upload shoe dataset to environment
2. Run data preprocessing and augmentation
3. Train custom CNN architectures
4. Implement transfer learning approaches
5. Compare model performances
6. Generate classification reports

### Q2 - Image Quality Assessment
1. Install quality assessment libraries
2. Load test images
3. Implement BRISQUE and PIQE metrics
4. Compare quality scores across images
5. Visualize quality assessment results

### Q3 - Airplane Detection/Segmentation
1. Prepare airplane dataset with annotations
2. Implement U-Net architecture
3. Train segmentation model
4. Evaluate detection performance
5. Visualize segmentation results

## Results and Performance
- **Shoe Classification**: Achieved high accuracy across multiple shoe categories
- **Quality Assessment**: Successfully discriminated between high and low quality images
- **Airplane Segmentation**: Accurate pixel-level airplane segmentation with good IoU scores
- **Transfer Learning**: Demonstrated significant performance improvements over training from scratch

## Model Architectures

### Custom CNN for Shoe Classification
- Input layer: 150×150×3 (RGB images)
- Conv2D layers with increasing filter sizes (16→32→64)
- MaxPooling for spatial reduction
- Fully connected layers with dropout
- Output: Softmax for multi-class classification

### U-Net for Airplane Segmentation
- Encoder: Downsampling path with skip connections
- Decoder: Upsampling path with feature concatenation
- Output: Sigmoid activation for binary segmentation
- Loss: Combined Dice loss and binary cross-entropy