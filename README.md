# Computer Vision Course - Complete Assignment Collection

## 🎯 Overview
This repository contains a comprehensive collection of Computer Vision assignments covering fundamental image processing techniques, deep learning applications, and advanced generative models. The coursework demonstrates a complete learning journey from traditional computer vision methods to state-of-the-art deep learning approaches.

## 📁 Project Structure
```
├── Vision/                          # Traditional Computer Vision Methods
│   └── HW1/
│       ├── src/
│       │   └── HW1_Vision_RashinRahnamoun_400243092.ipynb
│       ├── report.pdf
│       └── README.md
├── HW2/                            # Deep Learning Applications  
│   ├── Q1/
│   │   └── HW2_Vision_Q1(1).ipynb        # CNN Shoe Classification
│   ├── Q2/
│   │   └── Vision_HW2_Q2(2).ipynb        # Image Quality Assessment
│   ├── Q3/
│   │   ├── HW2_Vision_Q3_2.ipynb         # Airplane Detection & Segmentation
│   │   └── HW2_Vision_Q3(1).ipynb
│   ├── report.pdf
│   └── README.md
├── HW3/                            # Advanced Generative Models
│   ├── HW4_Q1_Final2_Vision.ipynb       # Variational Autoencoders (VAE)
│   ├── HW4_vision_Q2_Final2.ipynb       # Generative Adversarial Networks (GAN)
│   ├── HW4_Final_Q4_ver2.ipynb          # Denoising Diffusion Models (DDPM)
│   ├── Colab_vision_Q3_Final.ipynb
│   ├── Report_400243092_RashinRahnamoun.pdf
│   └── README.md
└── README.md                       # This file
```

## 🚀 Course Progression

### Phase 1: Traditional Computer Vision (Vision/HW1)
**Foundation Building**
- **Text Extraction**: OCR techniques for license plate recognition
- **Object Detection**: Star counting in astronomical images  
- **Core Skills**: Image preprocessing, morphological operations, contour analysis

**Technologies**: OpenCV, EasyOCR, Tesseract

### Phase 2: Deep Learning Applications (HW2)
**Neural Network Mastery**
- **CNN Classification**: Multi-class shoe classification with custom architectures
- **Transfer Learning**: Leveraging pre-trained models for improved performance
- **Quality Assessment**: Image quality metrics (BRISQUE, PIQE)
- **Segmentation**: U-Net for airplane detection and pixel-level segmentation

**Technologies**: TensorFlow/Keras, PyTorch, FastAI, Advanced CNN architectures

### Phase 3: Generative AI (HW3)
**Cutting-Edge Generative Models**
- **VAE**: Variational Autoencoders for latent space learning
- **GAN**: Deep Convolutional GANs for high-quality synthesis
- **DDPM**: Denoising Diffusion Probabilistic Models for state-of-the-art generation

**Technologies**: PyTorch, Advanced architectures (U-Net, ResNet blocks), Attention mechanisms

## 🎓 Learning Outcomes

### Technical Skills Acquired
- **Computer Vision Fundamentals**
  - Image preprocessing and enhancement
  - Feature extraction and object detection
  - Morphological operations and filtering
  
- **Deep Learning Expertise**
  - CNN architecture design and optimization
  - Transfer learning and fine-tuning strategies
  - Loss function design and training techniques
  
- **Generative AI Mastery**
  - Variational inference and latent space modeling
  - Adversarial training dynamics and stability
  - Diffusion processes and denoising networks

### Mathematical Foundations
- **Probability Theory**: Bayesian inference, variational methods
- **Optimization**: Gradient descent, Adam optimizer, learning rate scheduling
- **Information Theory**: KL divergence, mutual information
- **Signal Processing**: Fourier transforms, convolution operations

### Research and Development Skills
- **Experimental Design**: Hyperparameter tuning, ablation studies
- **Performance Evaluation**: Metrics design and comparative analysis
- **Visualization**: Result presentation and model interpretation
- **Documentation**: Technical writing and reproducible research

## 🛠 Technical Stack

### Core Libraries
- **Deep Learning**: PyTorch, TensorFlow/Keras, FastAI
- **Computer Vision**: OpenCV, PIL/Pillow, scikit-image
- **Scientific Computing**: NumPy, SciPy, pandas
- **Visualization**: Matplotlib, Seaborn, Plotly
- **Quality Assessment**: BRISQUE, PIQE, specialized metrics

### Advanced Components
- **Neural Architectures**: U-Net, ResNet, Attention mechanisms
- **Optimization**: Advanced optimizers, learning rate schedulers
- **Evaluation**: Custom metrics, statistical analysis tools
- **Data Processing**: Augmentation, normalization, preprocessing pipelines

## 📊 Key Achievements

### HW1 Results
✅ **Text Extraction**: >95% accuracy on license plate recognition  
✅ **Star Detection**: Robust counting across varying image conditions  
✅ **Algorithm Optimization**: Parameter tuning for maximum performance

### HW2 Results  
✅ **CNN Classification**: High accuracy multi-class shoe classification  
✅ **Transfer Learning**: Significant performance improvements over baseline  
✅ **Quality Assessment**: Effective discrimination between image qualities  
✅ **Segmentation**: Accurate pixel-level airplane detection with good IoU

### HW3 Results
✅ **VAE**: Clear latent space organization with smooth interpolation  
✅ **GAN**: High-quality image synthesis without mode collapse  
✅ **DDPM**: State-of-the-art generation quality with classifier-free guidance

## 🚀 Getting Started

### Prerequisites
```bash
# Python environment setup
python >= 3.8
pip install torch torchvision tensorflow opencv-python
pip install matplotlib seaborn pandas scikit-learn
pip install pillow easyocr brisque piqe
```

### Quick Start Guide
1. **Clone Repository**
   ```bash
   git clone <repository-url>
   cd computer-vision-course
   ```

2. **Environment Setup**
   ```bash
   pip install -r requirements.txt  # Install dependencies
   ```

3. **Choose Your Path**
   - **Beginner**: Start with `Vision/HW1` for fundamentals
   - **Intermediate**: Jump to `HW2` for deep learning
   - **Advanced**: Explore `HW3` for generative models

4. **Run Notebooks**
   - Open Jupyter notebooks in your preferred environment
   - Follow step-by-step implementations
   - Experiment with parameters and architectures

## 📈 Performance Metrics

### Model Comparison
| Assignment | Task | Best Model | Accuracy/Quality |
|------------|------|------------|------------------|
| HW1 Q1 | Text Extraction | EasyOCR + Preprocessing | 95%+ |
| HW1 Q2 | Star Counting | Morphological + Contour | Robust Detection |
| HW2 Q1 | Shoe Classification | Transfer Learning CNN | 90%+ |
| HW2 Q2 | Quality Assessment | BRISQUE + PIQE | Effective Discrimination |
| HW2 Q3 | Airplane Segmentation | U-Net | IoU > 0.8 |
| HW3 Q1 | VAE Generation | 2D/4D/16D Latent | Good Reconstruction |
| HW3 Q2 | GAN Synthesis | DCGAN | High Quality Images |
| HW3 Q4 | DDPM Generation | Conditional U-Net | SOTA Quality |

## 🎯 Future Extensions

### Potential Improvements
- **Advanced Architectures**: Vision Transformers, EfficientNet
- **Multi-Modal Learning**: Text-image fusion, CLIP integration  
- **Real-Time Applications**: Model optimization for deployment
- **Domain Adaptation**: Cross-domain generalization techniques

### Research Directions
- **Self-Supervised Learning**: Contrastive learning methods
- **Few-Shot Learning**: Meta-learning for computer vision
- **Explainable AI**: Attention visualization and model interpretation
- **Efficient Training**: Knowledge distillation and pruning techniques

## 👨‍🎓 About the Author
**Rashin Rahnamoun** - Student ID: 400243092

This collection represents a comprehensive journey through modern computer vision, demonstrating progressive learning from fundamental concepts to cutting-edge research implementations.

## 📄 License
This project is for educational purposes. Please refer to individual assignment requirements for specific usage guidelines.

---

*"Computer Vision is not just about making machines see, but about making them understand what they see."* - Course Philosophy