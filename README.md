# Deep Learning Model Compression 

This project focuses on optimizing and compressing deep learning models using **Pruning** and **Quantization** techniques. The primary goal is to reduce the model's size and complexity while maintaining its accuracy.

## Features
- Implementation of two pruning methods:
  - **One-shot Pruning:** Reduces model weights in a single step while maintaining acceptable accuracy.
  - **Step-by-step Pruning:** Gradually removes weights with retraining after each step, improving the model's accuracy and maintaining efficiency.
- **Quantization:** Compresses the model by reducing the bit-width of weights and activations, evaluated at 2, 4, 6, and 8 bits.
- Analysis of compression effects on accuracy and memory usage.

## Key Results
- **Pruning:**
  - One-shot pruning achieved a compression ratio with minimal accuracy loss.
  - Step-by-step pruning enabled higher compression with better accuracy recovery (up to 93.55%).
- **Quantization:**
  - Optimal balance found at 8-bit quantization with an accuracy of 93.24%.
  - Lower bit-widths (e.g., 2 bits) led to significant accuracy drops (85.81%).
- **Combined Pruning and Quantization:**
  - The final compressed model (40% pruned and 8-bit quantized) achieved 90.95% accuracy and a 4× reduction in model size.

## Dataset
- **Fashion-MNIST**: A dataset of 28×28 grayscale images, used for classification tasks.

## Prerequisites
- Basic understanding of Convolutional Neural Networks (CNNs).
- Python and PyTorch framework installed.
- Access to a runtime environment like Google Colab for running the code.

## How to Run
1. Clone the repository from [GitHub](https://github.com/Alighorbani1380).
2. Install the required dependencies listed in `requirements.txt`.
3. Follow the notebook steps to:
   - Train the CNN model.
   - Apply pruning and quantization techniques.
   - Analyze results and save the compressed model.

## Model Compression Results
| Technique          | Accuracy (%) | Compression Ratio | 
|--------------------|--------------|-------------------|
| Original Model     | 93.14        | -                 |
| Pruned Model       | 93.55        | 1.5×             |
| Quantized Model    | 93.24        | 4×               |
| Pruned + Quantized | 90.95        | 4×               |

