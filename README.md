# Conditional GAN for Virtual Cell Staining

## Problem Statement

Traditional microscopy imaging often requires multiple fluorescent stains to distinguish between different cell populations (e.g., dead vs. alive cells), which can be time-consuming, expensive, and potentially harmful to biological samples. This project addresses the challenge of **generating fluorescence microscopy images from brightfield images** using advanced deep learning techniques.

Our solution employs a **Conditional Generative Adversarial Network (cGAN)** to:
- Transform single-channel brightfield microscopy images into dual-channel fluorescence images
- Simultaneously predict both dead cell (ch1) and alive cell (ch2) fluorescence patterns
- Reduce the need for multiple fluorescent stains in cell viability analysis
- Accelerate microscopy workflows while maintaining high image quality

### Key Innovation
The model uses a **U-Net style generator** with dual outputs and a **Wasserstein GAN with Gradient Penalty (WGAN-GP)** training scheme to ensure stable training and high-quality synthetic fluorescence image generation.

## Research Background

This work is part of ongoing research in computational microscopy and deep learning applications in biological imaging. For detailed methodology, experimental results, and comprehensive analysis, please refer to the **Master's Thesis**: 

📖 **[Read the Full Master's Thesis](https://uu.diva-portal.org/smash/record.jsf?pid=diva2%3A1985518&dswid=-6328)**


## Features

- **🔬 Multi-Channel Generation**: Simultaneously generates dead and alive cell fluorescence
- **⚡ GPU Accelerated**: Optimized for CUDA-enabled training and inference
- **🎯 Advanced Training**: WGAN-GP implementation with gradient penalty for stable training
- **📊 Comprehensive Monitoring**: Real-time loss tracking and validation visualization
- **🔧 Robust Preprocessing**: Automated image organization, normalization, and tile extraction
- **📁 Smart Data Management**: Position-aware train/validation/test splitting to prevent data leakage

## Quick Start

### Prerequisites

- Python 3.8+
- CUDA-compatible GPU (recommended)
- 16GB+ RAM for large datasets

### Environment Setup

We've provided a complete conda environment specification to ensure reproducible results and avoid dependency conflicts:

The `conda_environment.yaml` file includes all necessary dependencies with pinned versions to ensure compatibility and reproducible results across different systems.

### Dataset Preparation

1. **Organize your microscopy images** in the following structure:

## Hardware Requirements

### Minimum Requirements
- GPU: 6GB VRAM (GTX 1060 or equivalent)
- RAM: 16GB system memory
- Storage: 50GB free space for datasets and models

### Recommended Requirements
- GPU: 12GB+ VRAM (RTX 3080 or better)
- RAM: 32GB system memory
- Storage: 100GB+ SSD storage

## Troubleshooting

### Common Issues

1. **CUDA Out of Memory**

2. **Import Errors**

3. **Data Loading Issues**


## Contributing

We welcome contributions to improve the model architecture, training stability, or evaluation metrics. Please:

1. Fork the repository
2. Create a feature branch
3. Implement your improvements
4. Add tests and documentation
5. Submit a pull request

## Citation

If you use this work in your research, please cite:
```@mastersthesis{Srivastava1985518,
   author = {Srivastava, Shivam},
   institution = {Uppsala University, Department of Information Technology},
   school = {Uppsala University, Department of Information Technology},
   title = {Conditional GenerativeAdversarial Networks for Virtual Cell Staining : A Novel Approach to Assessing Viability in 3D Brightfield Images},
   series = {IT},
   number = {mDV 25 022},
   keywords = {cGAN, Virtual cell staining, Deep Learning, Conditional Generative Adversarial Networks},
   abstract = {Cell viability assessment stands as a cornerstone methodology in modern biomedical research,with far-reaching implications across drug discovery pipelines, oncology studies, andtoxicological evaluations. The critical importance of accurate viability measurements cannot beoverstated, as these determinations directly influence experimental outcomes, therapeuticdevelopment timelines, and ultimately patient care decisions.Conventional approaches to viability assessment predominantly employ biochemical detectionmethods, which can be broadly categorized into three principal classes: (1) colorimetric assays(e.g., MTT, XTT), (2) fluorescence-based assays (e.g., Calcein-AM, propidium iodide), and (3)luminescence-based assays (e.g., ATP detection) . While these techniques have becomelaboratory mainstays, they carry significant limitations that researchers must carefully consider.Most notably, the very biological markers that enable detection often exhibit cytotoxic propertiesthemselves, creating a paradoxical situation where the measurement process may inadvertentlyalter the cellular state being measured. This delicate balance requires meticulous optimizationof reagent concentrations and strict temporal control during experimental protocols.In this thesis, I develop a conditional Generative Adversarial Network (cGAN) for virtual cellviability assessment. My original contributions include: (1) designing a novel dualoutputgenerator architecture that simultaneously predicts dead and alive cell distributions throughseparate decoder heads, improving SSIM by 18.7% compared to single-output baselines; (2)formulating a hybrid loss function combining adversarial loss (Ladv), perceptual loss (LV GG),and structural constraints (Lstruct), which reduced artifacts by 32% in ablation studies.The technical challenges associated with traditional viability assays extend beyond biologicalconsiderations. These methods frequently demand substantial time investments and laborintensive procedures, with multi-step protocols that may span several hours to days.The complexity of these workflows introduces numerous potential failure points - frominconsistent reagent handling to variability in incubation times - each capable of generatingexperimental artifacts that compromise data integrity. Furthermore, the endpoint nature of mostconventional assays provides only a single temporal snapshot, potentially missing dynamiccellular responses that could prove biologically or clinically relevant. },
   year = {2025}```
}


