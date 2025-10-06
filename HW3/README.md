# Computer Vision HW3 - Advanced Generative Models

## Overview
This homework assignment focuses on advanced generative models in computer vision, including Variational Autoencoders (VAE), Generative Adversarial Networks (GANs), and Denoising Diffusion Probabilistic Models (DDPM).

## Project Structure
```
HW3/
├── HW4_Q1_Final2_Vision.ipynb        # Variational Autoencoders (VAE)
├── HW4_vision_Q2_Final2.ipynb        # Generative Adversarial Networks (GANs)
├── HW4_Final_Q4_ver2.ipynb           # Denoising Diffusion Models (DDPM)
├── Colab_vision_Q3_Final.ipynb       # Additional implementations
└── Report_400243092_RashinRahnamoun.pdf  # Complete assignment report
```

## Assignment Questions

### Question 1: Variational Autoencoders (VAE)
**File**: `HW4_Q1_Final2_Vision.ipynb`

- **Objective**: Implement and analyze VAE for image generation and representation learning
- **Dataset**: MNIST handwritten digits
- **Key Components**:
  - Encoder network (recognition model)
  - Decoder network (generative model)
  - Reparameterization trick
  - KL divergence regularization

**Implementation Details**:
- **Architecture**: Fully connected encoder-decoder with bottleneck latent space
- **Latent Dimensions**: Experiments with 2D, 4D, and 16D latent spaces
- **Loss Function**: Reconstruction loss + KL divergence
- **Visualization**: t-SNE plots for high-dimensional latent spaces
- **Analysis**: Latent space interpolation and generation quality

**Key Techniques**:
- Variational inference for latent variable models
- Reparameterization trick for gradient flow
- Multi-dimensional latent space analysis
- t-SNE visualization for dimensionality reduction
- Reconstruction quality evaluation

### Question 2: Generative Adversarial Networks (GANs)
**File**: `HW4_vision_Q2_Final2.ipynb`

- **Objective**: Train GAN models for high-quality image synthesis
- **Architecture**: Deep Convolutional GANs (DCGANs)
- **Dataset**: Custom dataset for image generation

**Implementation Details**:
- **Generator**: Transposed convolutions for upsampling
- **Discriminator**: Convolutional layers for binary classification
- **Training**: Adversarial minimax training
- **Optimization**: Adam optimizer with careful learning rate tuning
- **Evaluation**: Generated image quality assessment

**Key Techniques**:
- Adversarial training dynamics
- Generator and discriminator architecture design
- Training stability techniques
- Mode collapse prevention
- Image quality evaluation metrics

### Question 3: Denoising Diffusion Probabilistic Models (DDPM)
**File**: `HW4_Final_Q4_ver2.ipynb`

- **Objective**: Implement DDPM for high-quality image generation
- **Dataset**: CIFAR-10 for conditional generation
- **Architecture**: U-Net with attention mechanisms

**Implementation Details**:
- **Forward Process**: Gradual noise addition over T timesteps
- **Reverse Process**: Learned denoising network
- **U-Net Architecture**: Skip connections and contextual embeddings
- **Conditioning**: Class-conditional generation
- **Sampling**: Classifier-free guidance for improved quality

**Key Components**:
- **Noise Scheduler**: Linear beta schedule for diffusion process
- **Context U-Net**: Time and class conditioning
- **Residual Blocks**: Feature extraction with skip connections
- **Attention Mechanisms**: Self-attention for global context
- **Classifier-Free Guidance**: Enhanced conditional generation

## Advanced Techniques Implemented

### VAE Specific
1. **Reparameterization Trick**
   ```python
   def reparameterize(self, mu, log_var):
       std = torch.exp(0.5 * log_var)
       eps = torch.randn_like(std)
       return mu + eps * std
   ```

2. **ELBO Loss Function**
   - Reconstruction loss: Binary cross-entropy
   - KL divergence: Regularization term
   - β-VAE variants for disentanglement

### GAN Specific
1. **Generator Architecture**
   - Transposed convolutions for upsampling
   - Batch normalization for training stability
   - Tanh activation for output normalization

2. **Discriminator Architecture**
   - Strided convolutions for downsampling
   - Leaky ReLU activations
   - Dropout for regularization

3. **Training Techniques**
   - Alternating generator/discriminator updates
   - Label smoothing for improved training
   - Spectral normalization for Lipschitz constraint

### DDPM Specific
1. **Diffusion Schedule**
   ```python
   def ddpm_schedules(beta1, beta2, T):
       betas = torch.linspace(beta1, beta2, T)
       alphas = 1 - betas
       alpha_bars = torch.cumprod(alphas, dim=0)
       return {
           'betas': betas,
           'alphas': alphas, 
           'alpha_bars': alpha_bars
       }
   ```

2. **U-Net with Time Embedding**
   - Positional encoding for timestep information
   - Cross-attention for conditional information
   - Skip connections for feature preservation

## Key Learning Outcomes
- **Generative Modeling**: Understanding different approaches to image generation
- **Variational Inference**: Mathematical foundations of VAEs
- **Adversarial Training**: GAN training dynamics and stability
- **Diffusion Processes**: Forward and reverse diffusion mathematics
- **Conditional Generation**: Class-conditional and text-conditional synthesis
- **Evaluation Metrics**: FID, IS, and perceptual quality assessment
- **Architecture Design**: Specialized networks for generative tasks

## Performance Analysis

### VAE Results
- **2D Latent Space**: Clear cluster formation for different digits
- **Higher Dimensions**: Better reconstruction quality with t-SNE visualization
- **Generation Quality**: Smooth latent space interpolation
- **Trade-offs**: Reconstruction vs regularization balance

### GAN Results
- **Training Stability**: Successful convergence without mode collapse
- **Image Quality**: High-resolution, realistic image generation
- **Diversity**: Good coverage of data distribution
- **Challenges**: Careful hyperparameter tuning required

### DDPM Results
- **Generation Quality**: State-of-the-art image synthesis quality
- **Conditional Generation**: Accurate class-conditional synthesis
- **Sampling**: Flexible sampling with guidance control
- **Training**: Stable training without adversarial dynamics

## Dependencies
- PyTorch
- Torchvision
- NumPy
- Matplotlib
- Seaborn
- Pandas
- Scikit-learn (for t-SNE)
- Tqdm (for training progress)
- PIL (Pillow)
- OpenCV

## Usage Instructions

### VAE Training and Analysis
1. Load MNIST dataset with appropriate transforms
2. Define VAE architecture with specified latent dimensions
3. Train with ELBO loss function
4. Visualize latent space and reconstructions
5. Generate new samples from prior distribution

### GAN Training
1. Prepare dataset and data loaders
2. Initialize generator and discriminator networks
3. Implement adversarial training loop
4. Monitor training stability and loss curves
5. Generate and evaluate synthetic images

### DDPM Implementation
1. Set up CIFAR-10 dataset for conditional training
2. Implement U-Net with time and class conditioning
3. Define forward and reverse diffusion processes
4. Train denoising network over multiple timesteps
5. Sample new images with classifier-free guidance

## Model Architectures

### VAE Architecture
- **Encoder**: [784] → [400] → [latent_dim × 2] (μ and σ)
- **Decoder**: [latent_dim] → [400] → [784]
- **Activation**: ReLU (hidden), Sigmoid (output)

### GAN Architecture
- **Generator**: [noise_dim] → [conv_transpose layers] → [3×64×64]
- **Discriminator**: [3×64×64] → [conv layers] → [1] (real/fake)

### DDPM U-Net
- **Input**: Noisy image + timestep + class condition
- **Architecture**: Encoder-decoder with skip connections
- **Output**: Predicted noise at given timestep
- **Features**: 128-256 feature channels with attention